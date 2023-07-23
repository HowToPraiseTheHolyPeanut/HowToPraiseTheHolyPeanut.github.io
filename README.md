<html>
  <head>
    <style>
    /* Ustawienia globalne */
    @import url('https://fonts.googleapis.com/css?family=Open+Sans');
    body {
      font-family: 'Open Sans', sans-serif;
      margin: 0;
      padding: 0;
      background-image: linear-gradient(to bottom, #202020, #FF8C42);
      color: #fff;
    }
 
      @keyframes fade-in {
  0% { opacity: 0; }
  100% { opacity: 1; }
}

h1, h2, ul {
  animation: fade-in 1s ease;
}      
    

    .hover-box:hover h2 {
      color: #000;
    }

      
    /* Nagłówki */
    h1, h2 {
      font-weight: bold;
      text-align: center;
      margin-top: 30px;
    }

    header {
      display: none;
    }


    h1 {
      font-size: 3em;
      text-shadow: 2px 2px #ccc;
    }

    a {
      color: black;
      text-decoration: none;    
  }

    a:hover {
      color: black;
      text-decoration: underline;
    }


    .hover-box:hover {
      background-color: #fff;
      color: #000;
    }
    
    h2 {
      font-size: 2em;
      border-bottom: 1px solid #ccc;
      padding-bottom: 10px;
      margin-bottom: 20px;
    }

    /* Lista */
    ul {
      list-style: none;
      margin: 0;
      padding: 0;
      text-align: center;
    }

    ul li.programming {
      background-color: #145369;
      color: #fff;
    }

    ul li.hobby {
      background-color: #e74c3c;
      color: #fff;
    }

    ul li:hover {
      background-color: #fff;
      color: #145369;
      border-color: #145369;
    }

      
    ul li {
      display: inline-block;
      margin: 10px;
      font-weight: bold;
      border: 2px solid #ccc;
      border-radius: 10px;
      padding: 10px;
      transition: background-color 0.3s ease;
    }

    ul li:hover {
      background-color: #fff;
      color: #145369;
      border-color: #145369;
    }
    a:hover {
      text-decoration: underline;
    }

    /* Paragrafy */
    p {
      font-size: 1.2em;
      line-height: 1.5;
      margin: 20px;
      text-align: justify;
    }



    </style>
  </head>
  <body>


    <script>
    async function updateCurrentlyPlaying() {
        const clientId = '9040b077e835427b905ae01e299b6b4b'; // Podstaw tutaj swoje Client ID z Spotify Developer Dashboard
        const token = 'ae319ad5f7c64559b8e359cd5e069bcd'; // Tutaj umieść token dostępu

        try {
            // Pobierz dane o aktualnie odtwarzanym utworze
            const response = await fetch('https://api.spotify.com/v1/me/player/currently-playing', {
                headers: {
                    'Authorization': 'Bearer ' + token,
                    'Content-Type': 'application/json'
                }
            });

            if (response.ok) {
                const data = await response.json();
                const trackName = data.item.name;
                const artistName = data.item.artists.map(artist => artist.name).join(', ');
                const albumName = data.item.album.name;

                // Aktualizuj zawartość diva "spotify-info" z pobranymi danymi
                document.getElementById('track-name').innerText = trackName;
                document.getElementById('artist-name').innerText = artistName;
                document.getElementById('album-name').innerText = albumName;
            } else {
                // Jeśli nie masz aktualnie odtwarzanego utworu, wyświetl informację
                document.getElementById('track-info').innerText = 'Nie odtwarzam żadnego utworu.';
                document.getElementById('album-info').style.display = 'none'; // Ukryj informacje o albumie
            }
        } catch (error) {
            console.error('Wystąpił błąd:', error);
            // Wyświetl informację o błędzie na stronie
            document.getElementById('spotify-info').innerText = 'Wystąpił błąd podczas pobierania danych z Spotify.';
        }
    }

    // Wywołaj funkcję updateCurrentlyPlaying, aby na początku załadowania strony od razu wyświetlić aktualnie odtwarzany utwór
    updateCurrentlyPlaying();
</script>




    <h1><b>coś</b></h1>
    <br>
    <h1>O mnie :></h1>
    <p>LvL 16, uczeń Technikum 2 klasy. W skrócie programista z dużymi ambicjami :> </p>
    <br>
    <h2>Języki Programowania których się uczę: </h2>
    <ul>
      <li><a href="https://howtopraisetheholypeanut.github.io/Python/">Python</a></li>
      <li>PHP</li>
      <li>JS</li>
      <li>C</li>
      <li>C++</li>
      <li>C#</li>
      <li>Batch</li>
      <li>Kotlin</li>
      <li>SQL</li>
    </ul>
  <br>
    <h2>Hobby</h2>
    <p>Ogólnie to uwielbiam Airsoft. Byłem na paru rozgrywkach i było super. Czasami próbuję swoich sił w Programowaniu Obiektowym, zajmując się różnymi grami. Oczywiście uwielbiam też grać. </p>
    <ul>
      <li>Airsoft</li>
      <li>GameDev</li>
      <li>Granie</li>
    </ul>
  <br>
    <h2>Co jest Grane?</h2>
 <ul>
      <li>SCP:SL <400 godzin></li>
      <li>CS:GO <400 godzin></li>
      <li>Minecraft</li>
    </ul>

  <div id="spotify-info">
        <h2>Aktualnie słucham:</h2>
        <p id="track-info">Tytuł: <span id="track-name">-</span>, Wykonawca: <span id="artist-name">-</span></p>
        <p id="album-info">Album: <span id="album-name">-</span></p>
  </div>
  
  <br>
  </body>
</html>

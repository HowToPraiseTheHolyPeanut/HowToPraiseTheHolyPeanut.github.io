<html>
  <head>
    <style>
    /* Ustawienia globalne */
    @import url('https://fonts.googleapis.com/css?family=Open+Sans');
    body {
      font-family: 'Open Sans', sans-serif;
      margin: 0;
      padding: 0;
      background-image: linear-gradient(to bottom, #333, #444);
      color: #fff;
    }
 
      @keyframes fade-in {
  0% { opacity: 0; }
  100% { opacity: 1; }
}

h1, h2, ul {
  animation: fade-in 1s ease;
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
    <br>
    <h1>O mnie :></h1>
    <p>Lvl 16, uczeń Technikum 2 klasy. W skrócie programista z dużymi ambicjami :> </p>
    <br>
    <h2>Języki Programowania których się uczę: </h2>
    <ul>
      <li><a href="">Python</a></li>
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
  <br>
  </body>
</html>

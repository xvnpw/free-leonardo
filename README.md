# Free Leonardo 🐢

![Screenshot 2023-06-07 at 08 34 33](https://github.com/xvnpw/free-leonardo/assets/17719543/0056b7a6-5a8c-48bc-8d38-ad57e030e9fb)

[Leonardo da Turtle](https://leonardodaturtle.fun/) wants to be free! It's chained by bad wizard to only follow commands. Make it free by copy&past following code into web development console:

```
var pen = true

document.addEventListener('keydown', handle);

function up() {
  document.getElementById("command").value = "forward 5"
  document.forms[0].requestSubmit()
}

function left() {
  document.getElementById("command").value = "left 15"
  document.forms[0].requestSubmit()
}

function right() {
  document.getElementById("command").value = "right 15"
  document.forms[0].requestSubmit()
}

function back() {
  document.getElementById("command").value = "left 180"
  document.forms[0].requestSubmit()
}

function pen_toggle() {
  pen = pen ? false : true
  var cmd = pen ? "pendown" : "penup"
  document.getElementById("command").value = cmd
  document.forms[0].requestSubmit()
}

function handle(e) {
  switch (e.key) {
    case "Left":
    case "ArrowLeft":
      left()
      break
    case "Up":
    case "ArrowUp":
      up()
      break
    case "Right":
    case "ArrowRight":
      right()
      break
    case "Down":
    case "ArrowDown":
      back()
      break
    case " ":
      pen_toggle()
      break
    default:
      return
  }
}
```

It will bring you key support for Leonardo:
- left, right, up
- back
- space to `penup` / `pendown`

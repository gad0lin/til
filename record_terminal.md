Install  asciinema:

```
pip3 install asciinema
```

Use asciicast2gif to create gif from it.

Handy functions:
```
function arc() {
   asciinema rec ~/tmp/asci/$1.cast
}
function arr() {
  cd ~/tmp/asci
  docker run --rm -v $PWD:/data asciinema/asciicast2gif -s 2 -t solarized-dark  $1.cast  $1.gif
}

function arm() {
   rm ~/tmp/asci/$1.cast
}
```

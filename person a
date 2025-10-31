<!DOCTYPE html>
<html>
<head>
<title>Person A Chat</title>
<link rel="stylesheet" href="style.css">
</head>
<body>
<h2>🔐 Person A</h2>

<textarea id="msgA" placeholder="Type a message"></textarea><br>
<input type="password" id="keyA" placeholder="Encryption key">
<button onclick="sendA()">Encrypt & Copy</button>

<label>Encrypted message:</label>
<textarea id="encA" readonly></textarea>

<hr>

<label>Paste Encrypted Msg From B:</label>
<textarea id="msgFromB"></textarea>
<input type="password" id="decKeyA" placeholder="Decryption key">
<button onclick="decryptA()">Decrypt</button>

<textarea id="decA" readonly></textarea>

<script>
function simpleEncrypt(t, k){let e="";for(let i=0;i<t.length;i++){e+=String.fromCharCode(t.charCodeAt(i)^k.charCodeAt(i%k.length));}return btoa(e);}
function simpleDecrypt(t, k){let d=atob(t),e="";for(let i=0;i<d.length;i++){e+=String.fromCharCode(d.charCodeAt(i)^k.charCodeAt(i%k.length));}return e;}

function sendA(){
  let enc = simpleEncrypt(msgA.value, keyA.value);
  encA.value = enc;
  navigator.clipboard.writeText(enc);
  alert("Encrypted message copied! Send it to Person B");
}

function decryptA(){
  decA.value = simpleDecrypt(msgFromB.value, decKeyA.value);
}
</script>
</body>
</html>

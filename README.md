<!DOCTYPE html>
<html lang="ja">
<head>
<meta charset="UTF-8">
<title>ゆいのToDoアプリ</title>

<style>
body{
    font-family: sans-serif;
    text-align:center;
    background:#ffeef5;
}

h1{
    color:#ff4da6;
}

input{
    padding:8px;
}

button{
    padding:8px 12px;
    margin-left:5px;
}

li{
    margin:8px;
}
</style>
</head>

<body>

<h1>ゆいのToDoアプリ</h1>

<input id="task" placeholder="やることを書く">
<button onclick="addTask()">追加</button>

<ul id="list"></ul>

<script>
function addTask(){

    const task = document.getElementById("task").value;

    if(task === "") return;

    const li = document.createElement("li");
    li.textContent = task;

    document.getElementById("list").appendChild(li);

    document.getElementById("task").value = "";
}
</script>

</body>
</html>

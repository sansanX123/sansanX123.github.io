<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <style>
        body {
            perspective: 500;
        }

        ul {
            margin: 100px;
        }

        li {
            transform-style: preserve-3d;
            position: relative;
            float: left;
            transition: all 3s;
            list-style: none;
            width: 100px;
            height: 100px;
            animation: run 10s linear infinite;
        }

        div {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
        }
         
        @keyframes run {
            0% {
                transform: translateX(0);
            }
            100% {
                transform: translateX(1000px) rotate3d(1,1,1,3600deg);
            }

        }

        li div:nth-child(1) {
            transform: translateZ(50px);
            background-color: orange;
        }

        li div:nth-child(2) {
            transform: translateZ(-50px) rotateY(180deg);
            background-color: red;
        }

        li div:nth-child(3) {
            transform: translateY(-50px) rotateX(90deg);
            background-color: blue;
        }

        li div:nth-child(4) {
            transform: translateY(50px) rotateX(-90deg);
            background-color: pink;
        }

        li div:nth-child(5) {
            transform: translateX(-50px) rotateY(-90deg);
            background-color: black;
        }

        li div:nth-child(6) {
            transform: translateX(50px) rotateY(90deg);
            background-color: #ccc;
        }
    </style>
</head>

<body>
    <ul>
        <li>
            <div></div>
            <div></div>
            <div></div>
            <div></div>
            <div></div>
            <div></div>
        </li>
    </ul>
</body>

</html>

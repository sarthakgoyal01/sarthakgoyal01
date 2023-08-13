<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculator</title>

    <link rel="stylesheet" href="style.css">
</head>
<body>

    <section class="calculator">
        <form type="text">
            <input type="text" class="screen">
        </form>

        <div class="buttons">
            <button type="button" class="btn btn-yellow" data-num="*">*</button>
            <button type="button" class="btn btn-yellow" data-num="/">/</button>
            <button type="button" class="btn btn-yellow" data-num="-">-</button>
            <button type="button" class="btn btn-yellow" data-num="+">+</button>


            <button type="button" class="btn btn-grey" data-num="9">9</button>
            <button type="button" class="btn btn-grey" data-num="8">8</button>
            <button type="button" class="btn btn-grey" data-num="7">7</button>
            <button type="button" class="btn btn-grey" data-num="6">6</button>
            <button type="button" class="btn btn-grey" data-num="5">5</button>
            <button type="button" class="btn btn-grey" data-num="6">6</button>
            <button type="button" class="btn btn-grey" data-num="4">4</button>
            <button type="button" class="btn btn-grey" data-num="3">3</button>
            <button type="button" class="btn btn-grey" data-num="2">2</button>
            <button type="button" class="btn btn-grey" data-num="1">1</button>
            <button type="button" class="btn btn-grey" data-num="0">0</button>

            <button type="button" class="btn btn-equal" data-num="">=</button>
            <button type="button" class="btn btn-clear" data-num="">C</button>


        </div>
    </section>

    <script src="main.js"></script>
</body>
</html>
(function(){
    let screen = document.querySelector('.screen');
    let buttons = document.querySelectorAll('.btn');
    let clear = document.querySelector('.btn-clear');
    let equal = document.querySelector('.btn-equal');

    buttons.forEach(function(button){
        button.addEventListener('click', function(e){
            let value = e.target.dataset.num;
            screen.value +=value;
        })
    });

    equal.addEventListener('click', function(e){
        if(screen.value === '='){
            screen.value = "";

        }else{
            let answer = eval(screen.value);
            screen.value = answer;
        }
    });

    clear.addEventListener('click', function(e){
        screen.value = "";
    });
})();
@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,400;0,500;0,600;0,700;0,800;0,900;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');


*{
    padding: 0;
    margin: 0;
    box-sizing: border-box;
}

body{
    min-height: 100vh;
    background: #efeff2;
    display: flex;
    justify-content: center;
    align-items: center;
}

.calculator{
    width: 300px;
    height: 500px;
    box-shadow: 4px 4px 30px rgba(0, 0, 0, 0.5);
    border-radius: 12px;
    background: #22252d;
    overflow: hidden;
}

form input{
    width: 100%;
    height: 150px;
    border: none;
    border-radius: 12px;
    font-size: 2rem;
    padding: 1rem;
    color: #fff;
    background: #000;
    text-align: right;
    pointer-events: none;
}

.buttons{
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    padding: 20px;
}

button{
    flex: 0 0 22%;
    margin: 5px 0;
    border: 1px solid black;
    width: 60px;
    height: 52px;
    font-size: 22px;
    font-weight: 600;
    border-radius: 5px;
    cursor: pointer;
}


.btn-yellow{
    background-color: rgb(245, 146, 62);
    color: #fff;
}

.btn-grey{
    background-color: rgb(224, 224, 224);
}

.btn-equal{
    background: green;
}

.btn-clear{
    background: red;
}
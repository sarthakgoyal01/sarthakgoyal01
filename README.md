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
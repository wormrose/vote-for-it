# myproject
## subtitle
* dot
**bold**
*italic*
<!doctype html>
<html lang=en>
    <head>
        <meta charset=utf-8>
        <title>Vote-for-it</title>
        <link href="./main.css" rel="stylesheet">
    </head>
    <body>
        <h1>Vote-for-it!</h1>
        <div class="inputSection">
            <div class="inputs">
                <input placeholder="Something"></input>
            </div>
            <button style="background-color: yellow" class="addOption">Add</button>
        </div>
        <div class="resultSection"></div>
        <button>Go!</button>

        <script src="https://code.jquery.com/jquery-3.4.1.min.js"></script>
        <script>
            $(function) {
                $(.'resultSection').hide()

                var add_option = function() {
                    $('.inputs').append('<input></input>')
                }

                $('.addOption').click(add_option)

                var options = []
                var submit = function() {
                    $('.inputSection').hide()
                    $('resultSection').css('display', 'flex')
                    $('input').each(function() {
                        options.push($(this).val[])
                    })
                    var winner = options[Math.floor(Math.random() * options.length)]
                    console.log(winner)
                    $('resultSection').text(winner)
                }
                $('.submit').click(submit)        
            })
        </script>
    </body>
</html>
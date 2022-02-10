# signin
<!DOCTYPE html>
<!--[if lt IE 7]>      <html class="no-js lt-ie9 lt-ie8 lt-ie7"> <![endif]-->
<!--[if IE 7]>         <html class="no-js lt-ie9 lt-ie8"> <![endif]-->
<!--[if IE 8]>         <html class="no-js lt-ie9"> <![endif]-->
<!--[if gt IE 8]>      <html class="no-js"> <!--<![endif]-->
<html>
    <head>
        <meta charset="utf-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <title></title>
        <meta name="description" content="">
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <link rel="stylesheet" href="">
    </head>
    <body>

        {% for message in messages  %}
        <div class = "alert alert- {{message.tags}} alert dismissable fade show" roles = "alert">
            <strong>Message:</strong>{{message}}
            <button type="button" class = "close" data-dismiss="alert" aria-label="Close">
            <span aria-hidden="true">&times;</span>
            </button>
        </div>
        {% endfor %} 

        <h3>SignUp</h3>
        <form action="/signup" method="post">
            {% csrf_token %}
            <label for="">Username</label>
            <input type="text" id="username" name ="username" placeholder="enter your username" required>
            <br>
            <label for="">password</label>
            <input type="password" id="pass1" name ="pass1" placeholder="enter your password" required>
            <br>
            <button type="submit">Sign In</button>
        </form>
        
        <script src="" async defer></script>
    </body>
</html>

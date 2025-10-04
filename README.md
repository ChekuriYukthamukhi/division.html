<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>example of div</title>
</head>
<body>
    <div>
        <h2>Contact Form </h2>
        <div style="background-color:whitesmoke; width:300px; height:200px;">
            
            <form action="/submit" method="post"> 

                <label for="name">Name:</label>
                <input type="text" id="name" name="name"><br><br>

                <label for="phone number">Phone Number:</label>
                <input type="tel" id="phone number" name="phone number" placeholder="10 digit number" pattern="[0-9][10]" inputmode="numeric" required aria-required="true"aria-required="phone-error" onkeypress="restrictAlphabets(event)">
                <span id="phone-error" role="alert"
                style="display: none;">numbers only.</span>">/span>

                <label for="email">Email:</label>
                <input type="email" id="email" name="email"><br><br>

                <label for="message">Message:</label><br>
                <textarea id="message" name="message" rows="4" cols="50">

                </textarea><br><br>
                <input type="submit" value="Submit"> 

            </form>
    </div>
    <script>
        function restrictAlphabets(event){
            const key = event.key;
            if (!/[0-9]/.test(key)&& key !== "Backspace" && key !== "ArrowLeft" && key !== "ArrowRight"){
                event.preventDefault();
                document.getElementById("phone-error").style.display = "inline";
            }else{
                document.getElementById("phone-error").style.display = "none";
            }
        }
    </script>
</body>
</html>

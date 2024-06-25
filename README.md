# primenumber

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Js Task 3</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC" crossorigin="anonymous">
    <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.9.2/dist/umd/popper.min.js" integrity="sha384-IQsoLXl5PILFhosVNubq5LC7Qb9DXgDA9i+tQ8Zj3iwWAwPtgFTxbJ8NT4GN1R8p" crossorigin="anonymous"></script>
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/js/bootstrap.min.js" integrity="sha384-cVKIPhGWiC2Al4u+LWgxfKTRIcfu0JTxR+EQDz/bgldoEyl4H0zUF0QKbrJ0EcQF" crossorigin="anonymous"></script>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/css/all.min.css" integrity="sha512-SnH5WK+bZxgPHs44uWIX+LLJAJ9/2PkPKZ5QiAj6Ta86w+fsb2TkcmfRyVX3pBnMFcV7oQPJkl9QevSCWr3W6A==" crossorigin="anonymous" referrerpolicy="no-referrer" />
<script>
    function prime(){
        const number=parseInt(document.forms.prime.primeNo.value);
        const primeresult=document.getElementById("primeresult");
        if(number<=1){
            primeresult.innerHTML=(number+" is not a prime number");
        }
        else if(number%2==0){
            primeresult.innerHTML=(number+" is not a prime number");
        }else{
            primeresult.innerHTML=(number+" is a prime number");
        }
        factorial()
    }
    function factorial(){
        let ans=1;
        const number=parseInt(document.forms.prime.primeNo.value);
        const fr=document.getElementById("factorialresult");
        if(number===0){
            fr.innerHTML=("Ans :" +ans);
        }
        let data="";
        for(let i=1;i<=number;i++){
            if(i==number){
                data +=i+" = ";
            }else{
                data +=i+" x ";
            }
            ans=ans*i;
        }
        data +=ans;
        fr.innerHTML=("Ans : " +data);
    }
</script>
<style>
    h4{
        color: white;
        text-align: center;
        padding-top: 20px;
        text-decoration:underline;
    }
    #result{
        border: 2px solid rgb(84, 235, 50);
        height: 50vh;
        color: white;
        font-weight: bolder;
    }
    #result>div:nth-child(odd){
        background-color: rgb(0, 122, 128);
    }
    #result>div:nth-child(even){
        background-color: rgb(26, 185, 92);
    }
    #factorialresult{
        /* overflow-x: scroll; */
    }
</style>
</head>
<body>
    <div class="container">
        <form id="prime">
            <div class="row ">
                <div class="col-4 m-auto">
                    <label>Enter Your Number</label>
                    <input type="text" name="primeNo" id="primeNo" class="form-control">
                </div>
                <div class="col-4 text-center m-auto">
                    <button class="btn btn-success btn-sm btn-block mt-4" type="button" onclick="prime()">Check Prime Number & Factorial</button>
                </div>
            </div>
        </form>
        <div class="row mt-5" id="result">
            <div class="col-6"><h4>Prime Number Result</h4><p id="primeresult"></p></div>
            <div class="col-6"><h4>Factorial Result</h4><p id="factorialresult"></p></div>
        </div>
    </div>
</body>
</html>

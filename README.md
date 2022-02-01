# calculadora
Proj de calculadora inicio


<!DOCTYPE html>
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>Calculadora</title>
  <style>
    *{ margin:0;
       padding: 0;
      
    }
    
    .fundo{
      background-image:linear-gradient(55deg,	#FF00FF, pink);
      height:100vh;
      color:#fff;
      font-family:Arial, Helvetica, sans-serif;
      text-align: center;
      }
   
    .calculadora{
    position:absolute;
    background-color:black;
    top:50%;
    left:50%;
    transform: translate(-50%,-50%);
    border-radius:15px;
    padding:15px;
    }
   .botao{
     width:50px;
     height:50px;
     font-size:25px;
     cursor:pointer;
     background-color:rgb(31,31,31);
     margin:2px;
     border:none;
     color:white;
   }
    
    .botao:hover{ background-color:pink;
      
    }
   #resultado{
     background-color:white;
     width: 207px;
     height: 30px;
     margin: 5px;
     font-size: 25px;
     text-align:right;
     padding: 5px;
     color:black;
     
     
   }
   
   #name{
     font-family: Helvetica;
     font-size: 30pt;
     color:skyblue;
     text-shadow: 2pt 2pt 2pt black;
      }
    
  </style>
 
</head>
<body>
  
 <div class="fundo">
   <h1 id=name>Gabrielly vila</h1>
   <div class="calculadora">
     <h1> Calculadora</h1>
   <p id="resultado"></p>
   
   <table>
     <tr>
       <td><button class="botao" onclick="clean('')">C</button></td>
       <td><button class="botao" onclick="back()"><</button></td>
       <td><button class="botao" onclick="insert('/')">/</button></td>
       <td><button class="botao" onclick="insert('*')">X</button></td>
       
     </tr>
     
      <tr>
       <td><button class="botao" onclick="insert('7')">7</button></td>
       <td><button class="botao"onclick="insert('8')">8</button></td>
       <td><button class="botao"onclick="insert('9')">9</button></td>
       <td><button class="botao" onclick="insert('-')">-</button></td>
        
      </tr>
      
      <tr>
       <td><button class="botao"onclick="insert('4')">4</button></td>
       <td><button class="botao"onclick="insert('5')">5</button></td>
       <td><button class="botao" onclick="insert('6')" >6</button></td>
       <td><button class="botao" onclick="insert('+')">+</button></td>
    
      </tr>
      
      <tr>
      <td><button class="botao" onclick="insert('1')">1</button></td>
       <td><button class="botao" onclick="insert('2')">2</button></td>
       <td><button class="botao" onclick="insert('3')">3</button></td>
       <td rowspan="2"><button onclick="calcular()" style=height:106px; class=botao>=</button></td>
       </tr>
       
       <tr>
       <td colspan="2"><button class="botao" onclick="insert('0')" style=width:106px;>0</button></td>
       <td><button class="botao"onclick="insert('.')">.</button></td>
         
       </tr>
      
     
    </table>
  
  
 </div>
   
 
  
  <script>
    function insert(num)
    {
    var numero = document.getElementById('resultado').innerHTML;
    
    document.getElementById('resultado').innerHTML = numero + num;
      }
    
    
      function clean()
    {
      document.getElementById('resultado').innerHTML="";
    }
    
    function back() 
    {
      var resultado=document.getElementById('resultado').innerHTML;
      document.getElementById('resultado').innerHTML = resultado.substring(0,resultado.length -1);
    }
    function calcular()
    {
      var resultado = document.getElementById('resultado').innerHTML;
      if(resultado)
    
    { 
      document.getElementById('resultado').innerHTML= eval(resultado);
    }
    
    else
    {
      document.getElementById('resultado').innerHTML= "Nada a calcular"
    }
  
  
    }
    
  </script>
  

</body>
</html>


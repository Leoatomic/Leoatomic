<svg>

<head>
   <title>Leoatomic</title>
</head>

<body onload="startTime()">
   <span style="text-align: left;" id="ora"></span>
   <span style="text-align: right;" id="data"></span>
</body>

<script>
   n = new Date();
   anno = n.getFullYear();
   mese = n.getMonth() + 1;
   giorno = n.getDate();
   document.getElementById("data").innerHTML = giorno + "/" + mese + "/" + anno;

   function startTime() {
      var today = new Date();
      var h = today.getHours();
      var m = today.getMinutes();
      var s = today.getSeconds();
      m = checkTime(m);
      s = checkTime(s);
      document.getElementById('ora').innerHTML =
         h + ":" + m + ":" + s;
      var t = setTimeout(startTime, 1000);
   }

   function checkTime(i) {
      if (i < 10) {
         i = "0" + i
      };
      return i;
   }
</script>

</svg>

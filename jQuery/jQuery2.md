```javascript
 <script src="https://cdn.staticfile.org/jquery/1.10.2/jquery.min.js">        //引入
    </script>
    <script>
        $(document).ready(function () {                                       			//使用
            $("div").hover(function (){
                $("div.myDiv").css({
                    "border-radius": "100px",
                    "border": "50px solid blue",
                    "border-left-color": "transparent",
                });
            }, function () {
                $("div.myDiv").css({
                    "borddhruvasagar/vim-table-modeer-width": "10px",
                    "border-radius": "100px",
                    "border": "50px solid blue"
                });
            });
        });
        var i = 0;
        setInterval(function () {
            $("div.myDiv").css("margin-left", i += 1);
            console.log(i);
            if (i >= 1920) {
                i = 0;
                // $("div.myDiv").css("margin-top",i+=100);
            }
            // if(i%)
        }, 1);
    </script>
```


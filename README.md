# JS_NextStepPagination
JavaScript jQuery Next step pagination 

```JS
 // Source: Paid jQuery Tutorial 
<html>
<head>
    <title>jQuery Complete Course</title>
</head>
<body>
    <h1>Welcome to jQuery Course</h1>
    <a href="http://www.google.com">Google</a>
    <form>
    <div class="content">
        <div class="step"><h1>First</h1>
            This is the first Page
            <div>
            <a href="#">Next</a>
            </div>
        </div>
        <div class="step hiddenStep">
            <h1>Second</h1>
            This is the second Page
            <div>
            <a href="#">Next</a>
            </div>
        </div>
        <div class="step hiddenStep">
            <h1>Third</h1>
            This is the third Page
            <div>
            <a href="#">Next</a>
            </div>
        </div>
    </div>
    </form>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
    <script>
    $(document).ready(function(){
        $('.hiddenStep').css('display','none');
        $('a[href="#"]').click(function(event){
            event.preventDefault();
            var parent = $(this).closest('.step');
            var mainContent = $('.content>.step');
            var index = mainContent.index(parent)+1;
            parent.css('display','none');
            mainContent.eq(index).css('display','block');
        })
        
    })

    </script>
</body>
</html>

```

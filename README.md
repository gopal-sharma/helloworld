
<!DOCTYPE html>
<html>
<head>
    <meta http-equiv="content-type" content="text/html; charset=UTF-8">
    <meta name="robots" content="noindex, nofollow">
    <meta name="googlebot" content="noindex, nofollow">
    <script type="text/javascript" src="//code.jquery.com/jquery-1.10.1.js"></script>
    <link rel="stylesheet" type="text/css" href="//cdnjs.cloudflare.com/ajax/libs/bootstrap-datepicker/1.3.0/css/datepicker.min.css">
    <script type="text/javascript" src="//cdnjs.cloudflare.com/ajax/libs/bootstrap-datepicker/1.3.0/js/bootstrap-datepicker.min.js"></script>



    <link rel="stylesheet" type="text/css" href="//netdna.bootstrapcdn.com/bootstrap/3.1.1/css/bootstrap.min.css">



    <script type="text/javascript" src="//netdna.bootstrapcdn.com/bootstrap/3.1.1/js/bootstrap.min.js"></script>



    <script type="text/javascript" src="//cdnjs.cloudflare.com/ajax/libs/moment.js/2.5.1/moment.min.js"></script>



    <script type="text/javascript" src="http://cdnjs.cloudflare.com/ajax/libs/bootstrap-datetimepicker/3.0.0/js/bootstrap-datetimepicker.min.js"></script>



    <script type="text/javascript" src="http://cdnjs.cloudflare.com/ajax/libs/moment.js/2.4.0/lang/en-gb.js"></script>



    <style type="text/css">

    </style>

    <title>Start / End Date Time Picker</title>







    <script type='text/javascript'>
    $(window).load(function(){
        jQuery(function () {
            jQuery('#startDate').datetimepicker();
            jQuery('#endDate').datetimepicker();
            jQuery("#startDate").on("dp.change",function (e) {
                e.date.minute(e.date.minute()-1);
                jQuery("#startDate input").val(e.date.format('MM/DD/YYYY h:mm a'));
                jQuery("#endDate input").val(new moment().format('MM/DD/YYYY h:mm a'));
            });
            jQuery("#startDate").on("dp.show",function (e) {
                e.date.minute(e.date.minute()-1);
                jQuery("#startDate input").val(e.date.format('MM/DD/YYYY h:mm a'));
                jQuery("#endDate input").val(new moment().format('MM/DD/YYYY h:mm a'));
            });
        });
    });
    </script>


</head>

<body>
<div class="container">
    <div class="col-sm-6" style="height:75px;">
        <div class='col-md-5'>
            <div class="form-group">
                <div>Start</div>

                <div class='input-group date' id='startDate'>
                    <input type='text' class="form-control" name="startDate" />
                    <span class="input-group-addon"><span class="glyphicon glyphicon-calendar"></span>
					</span>
                </div>
            </div>
        </div>
        <div class='col-md-5'>
            <div class="form-group">
                <div>End</div>

                <div class='input-group date' id='endDate'>
                    <input type='text' class="form-control" name="org_endDate" />
                    <span class="input-group-addon"><span class="glyphicon glyphicon-calendar"></span>
					</span>
                </div>
            </div>
        </div>
    </div>
</div>

</body>

</html>


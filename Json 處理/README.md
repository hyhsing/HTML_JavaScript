如果使用 Ajax 資料傳回Json時候

例如 
  $("#button").click(function(){
        $.ajax({            
            url: 'get_data',     
            type:'GET',
            dataType: 'json',
            data: { number: '00001' },
            timeout:3000,  
        success: function(data){
            $("#div1").html(data.name);
        },
        error: function(result){
            $("#div1").html('error');
        }  ,
        always: function(result){
            $("#div2").html('always');
        }   
        }
        
        );

 
    });

直接指定 data.name 則為 hash 指定
如果使用 JSON.stringify(data) 則轉回字串
如果使用 JSON.parse(data) 則將字串轉為JSON
如果使用 var obj = JSON.parse(JSON.stringify(data)) 則將 Json 值轉為字串然後再轉回來



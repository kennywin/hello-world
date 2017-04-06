# hello-world
$('#btn').click(function (){
			$.ajax({         
				url: 'ajax_output.php',
				cache: false,
				dataType: 'html',
					type:'GET',
				data: {
          //要 ''jquery''化的地方,可以在去蕪存菁的方式抓出欄位嗎?而不用日後若是有擴充表單欄位，則要一筆一筆手動列入欄位資訊.
					name: $('#name').val(),
					sex: $('#sex').val(),
					username: $('#username').val()
				},
				error: function(xhr) {
					alert('Ajax request 發生錯誤');
				},
				success: function(response) {
					$('#send_data').html(response);
				}
			});
		}); 

# Ajax-Function

 ajax(url, data, callBack, hasLoading, isHtml)
 <pre>
      url        : HTTP Request Url
      data  	 : HTTP Request Form Data
      callBack   : HTTP Response Data,
      loading    : During Process  Show Loading Message
      isHtml     : HTTP Response is HTML Format
 </pre>

 <pre>
      If HTTP Request is JSON Format
      Response Format  must be  like that { status: 1, message: "This is a ajax message", data: { Here array data}}
 </pre>

#Usage

Using sample : has loading true, isHtml false response is JSON

<pre>
    ajax('index.php', {id:'1'}, function (data) {
    		 /* Response JSON */
             console.log(data);
             console.log(data.myKey);
             console.log(data.myKey.id);
             console.log(data.myKey.name);
      }, true, false);
</pre>

  Using Sample  has loading true, isHtml true response is HTML
<pre>
  	ajax('index.php', {id:1}, function (data) {
   			/* Response HTML */
    	    console.log(data);
  	}, true, true);
</pre>
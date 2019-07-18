  # document.createFragment能解决document.createElement的渲染多个li重绘多次,影响性能的问题


  ```
	var fragment=document.createDocumentFragment();
	var ul=document.createElement("ul");
	var li=null;
	for(var i=0;i<3;i++){
	    li=document.createElement("li");
	    li.appendChild(document.createTextNode("item"+i));
	    ul.appendChild(li);
	}
	fragment.appendChild(ul);
	document.body.appendChild(fragment);

  ```
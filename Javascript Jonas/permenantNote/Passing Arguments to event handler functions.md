# Explanation

- short-cut you can't
- But we've a great way to do it using [](Apply,%20call,%20and%20Bind%20Methods.md#bind|bind)

    ```js
    const callbackArgumented=function(e, arg1){
    	// procedures
    	// to use arg1 use 'this'keyword
    	// if multiple elements pass them as an array
    }
    btn.addEventListener('click', callbackArgumented)// wrong You can't pass Arguments

    // callback for event only have one argument (e)⭐
    // do the following to pass arg1
    btn.addEventListener('click', callbackArgumented.bind(1));// will set arg1 whic
    ```

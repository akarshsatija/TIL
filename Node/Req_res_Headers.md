# How to limit requests from limited sources - CORS

    app.use(function(req, res, next) {
    	if (req.headers.origin && ((req.headers.origin.indexOf("//api.lbb.in") > -1) || (req.headers.origin.indexOf("//testapi.lbb.in") > -1) || (req.headers.origin.indexOf("//lbb.in") > -1) || (req.headers.origin.indexOf("//lbbnew.staging.wpengine.com") > -1))) { res.header("Access-Control-Allow-Origin", req.headers.origin); }
    	res.header("Access-Control-Allow-Headers", "X-Requested-With");
    	res.header('Access-Control-Allow-Credentials', true);
    	next();
    });

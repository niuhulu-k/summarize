
```javascript
// 该方法用来在文件加载之前改变文件
var ejs = require('ejs');
var UaParser = require('ua-parser-js');
var app = express();
// 引用html
app.set('views', 'dist');//设置视图的对应目录,views貌似是固定参数
app.set('view engine', 'html');//设置默认的模板引擎例如：html、ejs...
app.engine('html', ejs.__express); //定义模板引擎

////引用ejs
// app.set('views',"public");  //设置视图的对应目录
// app.set("view engine","ejs");       //设置默认的模板引擎
// app.engine('ejs', ejs.__express);       //定义模板引擎

app.get('/', function (req, res) {
    res.render('index', { title:  });//重新渲染
});

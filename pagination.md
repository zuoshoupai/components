### 分页样式（bootstrap 3.0提取）
![示例](http://img1.ph.126.net/RBurHqsl-MJZ1XVs60bjww==/1682375935900153387.png)
1. html部分

```html
<div class="pages">
 <ul class="pagination">
    <li class="disabled"><a href="#" aria-label="Previous"><span aria-hidden="true">&laquo;</span></a></li>
    <li class="active"><a href="#">1 <span class="sr-only">(current)</span></a></li>
    ...
  </ul>
</div>
```
2.  css部分

```css
.pages{display: flex;justify-content: center;}
.pagination { display: inline-block; padding-left: 0; margin: 20px 0; border-radius: 4px; }
.pagination li { display: inline; }
.pagination .disabled span,.pagination .active span{float: left;padding: 6px 12px;}
.pagination>.active>a, .pagination>.active>a:focus, .pagination>.active>a:hover, .pagination>.active>span, .pagination>.active>span:focus, .pagination>.active>span:hover {z-index: 3;color: #fff;cursor: default;background-color: #337ab7;border-color: #337ab7;}
.pagination li a { position: relative; float: left; padding: 6px 12px; margin-left: -1px; line-height: 1.428571429; text-decoration: none; background-color: #fff; border: 1px solid #ddd; }
.pagination li:first-child a { margin-left: 0; border-bottom-left-radius: 4px; border-top-left-radius: 4px; }
.pagination li:last-child a { border-top-right-radius: 4px; border-bottom-right-radius: 4px; }
.pagination li a:hover, .pagination li a:focus { background-color: #eee; }
.pagination .active a, .pagination .active a:hover, .pagination .active a:focus { z-index: 2; color: #fff; cursor: default; background-color: #428bca; border-color: #428bca; }
.pagination .disabled a, .pagination .disabled a:hover, .pagination .disabled a:focus { color: #999; cursor: not-allowed; background-color: #fff; border-color: #ddd; }
.pagination-lg li a { padding: 10px 16px; font-size: 18px; }
.pagination-sm li a, .pagination-sm li span { padding: 5px 10px; font-size: 12px; }
```
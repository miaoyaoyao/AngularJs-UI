# AngularJs Pagination -- Want to be the best Pagination 

Since name for a pagination is boring, so I decide name it to tm.I'm not good at English, wish you you catch what I said And help me improve my English.

## tm.pagination -- A very simple and useful pagination in AngularJs
Online demo [tm.pagination](http://demo.miaoyueyue.com/js/ng/AngularJs-UI/demo/pagination.html)

**relate blog articles:**

- https://www.miaoyueyue.com/archives/791.html
- https://www.miaoyueyue.com/archives/813.html
- https://www.miaoyueyue.com/archives/833.html

default:

<img src="http://www.miaoyueyue.com/wp-content/uploads/2014/08/9a8495c8f641da099fef6175acefb5d9.png" />

with some css and template change you can turn it to this

<img src="http://www.miaoyueyue.com/wp-content/uploads/2014/08/f12bb2987330a85ebbe5e3420fe9c773.png"/>

    // in the view
    <tm-pagination conf="paginationConf"></tm-pagination>

    // in the controller
    $scope.paginationConf = {
        currentPage: 1,
        totalItems: 8000,
        itemsPerPage: 15,
        pagesLength: 15,
        perPageOptions: [10, 20, 30, 40, 50],
        onChange: function(){

        }
    };

conf is a object, it has attributes like below:

*   currentPage: Current page number, default 1
*   totalItems: Total number of items in all pages
*   itemsPerPage:  number of items per page, default 15
*   onChange: when the pagination is change, it will excute the function
*   pagesLength: number for pagination size, default 9
*   perPageOptions: define select how many items in a page, default [10, 15, 20, 30, 50]

if you want to use with ajax,you may follow like this:

    $scope.paginationConf = {
        onChange: function() {
            $http.get('xxx', function(data) {
                $scope.paginationConf.totalItems = data.totalItems;
            })
        }
    };
    

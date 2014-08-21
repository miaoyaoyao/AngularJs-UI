# AngularJs UI -- Want to be the best UI

Since name for a UI is boring, so I decide name it to tm.I'm not good at English, wish you you catch what I said And help me improve my English.

## tm.pagination -- A very simple and useful pagination in AngularJs
On line demo [tm.pagination](http://demo.miaoyueyue.com/js/AngularJs-UI/demo/pagination.html)

    // in the view
    <tm-pagination conf="paginationConf"></tm-pagination>

    // in the controller
    $scope.paginationConf = {
        currentPage: 1,
        totalItems: 8000,
        itemsPerPage: 15,
        pagesLength: 15,
        perPageOptions: [10, 20, 30, 40, 50],
        rememberPerPage: 'perPageItems',
        onChange: function(){

        }
    };

conf is a object, it has attributes like below:

*   currentPage: Current page number, default 1
*   totalItems: Total number of items in all pages
*   itemsPerPage:  number of items per page, default 15
*   onChange: when the pagination is change, it will excute the function
*   pagesLength: number for pagination size, default 9
*   perPageOptions: defind select how many items in a page, default [10, 15, 20, 30, 50]
*   rememberPerPage: use to remember how many items in a page select by user.








# datatable_helper-extension

This Extension Provides Manage Your Datatables Easyly

You can include asset twig bundle

`{% include 'visiosoft.extension.datatable_helper::assets' %}`

You can directly use `dtHelper`

#### Setters
`dtHelper.setScrollCollapse(true);`

`dtHelper.setFilter(false);`

`dtHelper.setTableElement(tableName);`

`dtHelper.setDom(<"top"i>rt<"bottom"flp><"clear">);`

`dtHelper.setScrollY("30vh");`

#### Getters
`getData(element, data)`

`getButtons(buttons)`


#### Usage Example
```
let exampleTable = {
    element: $('#exampleTable'),
    filterElement: $('#exampleTable  thead th'),
        data: [
        {
            data: ((row) => {
                return row.data?.data || "-"
            }),
        },
        {
            data: ((row) => {
                return row.data?.data || "-"
            }),
        }
    ]
}

dtHelper.setScrollCollapse(true);
dtHelper.setFilter(false);
dtHelper.setTableElement(exampleTable);
activeTransactionsTable = dtHelper.initDataTable();

// Live Reload
setInterval(function () {
    exampleTable.ajax.reload()
}, 30000)

```


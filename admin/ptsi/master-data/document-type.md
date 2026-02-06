## Data Table

API untuk mengambil data table

---

## Endpoint
```
GET /api/admin/master-data/data/organization-type
```

---

## Headers
```
Authorization: Bearer {token}
Accept: application/json
```

---

## Response Berhasil (200 OK)
```json
{
    "draw": 0,
    "recordsTotal": 18,
    "recordsFiltered": 18,
    "data": [
        {
            "id": 1,
            "name": "BIRO",
            "created_at": "2020-07-31 00:57:43",
            "updated_at": "2021-01-26 17:32:46",
            "action": "<td>\r\n              <div class=\"btn-group ptsi-btn-action-dropdown\">\r\n                  <button type=\"button\" class=\"btn dropdown-toggle\"\r\n                          data-toggle=\"dropdown\" data-display=\"static\" aria-haspopup=\"true\" aria-expanded=\"false\">\r\n                      <span class=\"three-bullet-btn\"></span>\r\n                  </button>\r\n                  <div class=\"dropdown-menu dropdown-menu-right\">\r\n                      <button onclick=\"editData(1)\" class=\"dropdown-item\">\r\n                          <i class=\"fa fa-pencil\" aria-hidden=\"true\"></i>\r\n                          <span class=\"dropdown-item-text\">Edit Data</span>\r\n                      </button>\r\n                      <button onclick=\"deleteData(1)\" class=\"dropdown-item\">\r\n                          <i class=\"fa fa-trash\" aria-hidden=\"true\"></i>\r\n                          <span class=\"dropdown-item-text\">Delete Data</span>\r\n                      </button>\r\n                  </div>\r\n              </div>\r\n          </td>"
        },
    ],
    "queries": [
        {
            "query": "select count(*) as aggregate from (select '1' as `row_count` from `master_organization_type`) count_row_table",
            "bindings": [],
            "time": 1.24
        },
        {
            "query": "select * from `master_organization_type`",
            "bindings": [],
            "time": 0.52
        }
    ],
    "input": []
}
```
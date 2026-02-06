## Headers
```
Authorization: Bearer {token}
Accept: application/json
```


## Save User
# End Point
```
POST /api/master-data/data/user/save
```

# Payload
```json
{
    "name" => "",
    "group_user" => "",
    "nik" => "",
    "division" => "",
    "username" => "",
    "password" => "",
    "email" => "",
    "unit" => "",
    "role" => "",
    "status" => "",
    "activation_token" => "",
    "view_only" => "",
}
```

## Delete User
POST /api/master-data/data/user/delete/{id}

## Get User
GET /api/master-data/user/edit/{id}

# Sample Response 
```json
{
    "status": true,
    "message": "Success",
    "data": {
        "sidebar": "master-data",
        "user": {
            "id": 1,
            "name": "kincat only",
            "nik": "12345",
            "username": "kincat",
            "photo": "users/d2w17l0i7co78n2vqI9u8DFsIMtF0O6oAYS7yfQV.png",
            "email": "kincat@gmail.com",
            "role": "ADMIN",
            "division": "IT",
            "status": "ACTIVE",
            "deleted": 0,
            "activation_token": null,
            "group_user": "SUPER_ADMIN",
            "unit": null,
            "view_only": 0,
            "has_accept_pdp": null,
            "ptsi_sso_id": null,
            "created_at": "2020-07-10 21:22:14",
            "updated_at": "2025-11-19 15:57:26"
        },
        "group_user": "SUPER_ADMIN",
        "all_pa": [
            {
                "id": 1,
                "pengguna_anggaran": "SB INFRAS",
                "siho_cabang_db": "DB INFRAS",
                "status_office": "DIVISI BISNIS",
                "cabang_nav": null,
                "fungsi": "OPERASIONAL",
                "direktorat": "DIRKOM 2",
                "unit_head_ho": "INFRAS",
                "alias_name": null,
                "alamat": "Graha Surveyor Indonesia Lt. 7 Jl. Jend. Gatot Subroto Kav.56 - Jkt - 12950",
                "location": "Jakarta",
                "is_sentralisasi": "1",
                "created_at": "2020-11-19 05:08:10",
                "updated_at": "2020-11-19 05:10:39"
            },
        ],
        "user_pa": [
            {
                "id": 8216,
                "user_id": 1,
                "structure_id": 1,
                "entity": "SB INFRAS",
                "created_at": "2026-01-20 20:54:17",
                "updated_at": "2026-01-20 20:54:17"
            },
        ],
        "method": "Edit"
    }
}
```

## Update User
# End Point
```
POST /api/master-data/data/user/update/{id}
```

# Payload
```json
{
    "name" => "",
    "group_user" => "",
    "nik" => "",
    "division" => "",
    "username" => "",
    "password" => "",
    "email" => "",
    "unit" => "",
    "role" => "",
    "status" => "",
    "activation_token" => "",
    "view_only" => "",
}
```
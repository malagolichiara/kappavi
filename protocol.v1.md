# prorocol V1

## initial mindstorming

    {"set": {"anykey": "anyvalue"}}
    -> {"result": "ok"}
    -> {"result": "ko"}
    
    {"get": ["anykey1", "anykey2"}}
    -> {"result": ["anyvalue1","anyvalue2"]}
    -> {"result": ["anyvalue1",null]}
    -> {"result": [null,"anyvalue2"]}
    -> {"result": [null,null]}
    
    {"del": "anykey"}
    -> {"result": "ok"}
    -> {"result": "ko"}
    
    {"exists": "anykey"}
    -> {"result": 1}
    -> {"result": 0}

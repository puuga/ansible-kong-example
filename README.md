# ansible-kong-example
An example for managing Kong services with Ansible


    ansible-playbook play.yml  -e IPADD=IPADD      # IPADD is the kong Gateway ADMIN API's IP 
     
    
    PLAY [localhost] ***************************************************************

    TASK [setup] *******************************************************************
    ok: [localhost]

    TASK [kong_service : Check if service exists] **********************************
    ok: [localhost]

    TASK [kong_service : Create service] *******************************************
    ok: [localhost]

    TASK [kong_service : Update a service] *****************************************
    skipping: [localhost]

    TASK [kong_route : Get service ID] *********************************************
    ok: [localhost]

    TASK [kong_route : Fail if service ID cannot be found] *************************
    skipping: [localhost]

    TASK [kong_route : Create route] ***********************************************
    ok: [localhost]

    TASK [kong_plugins : Get service ID] *******************************************
    ok: [localhost]

    TASK [kong_plugins : Fail if service ID cannot be found] ***********************
    skipping: [localhost]

    TASK [kong_plugins : Create plugins] *******************************************
    ok: [localhost]

    TASK [kong_consumer : Get service ID] ******************************************
    ok: [localhost]
    
    TASK [kong_consumer : Fail if service ID cannot be found] **********************
    skipping: [localhost]

    TASK [kong_consumer : Create consumer] *****************************************
    ok: [localhost]

    TASK [kong_consumer : Create consumer Auth] ************************************
    ok: [localhost]

    PLAY RECAP *********************************************************************
    localhost                  : ok=10   changed=0    unreachable=0    failed=0   

    

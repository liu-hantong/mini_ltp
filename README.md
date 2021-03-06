```bash
export LD_LIBRARY_PATH=/home/lht/mini_ltp/ltp/i86-redhat/lib"
./ltp/i86-redhat/bin/ltpadmin
```

```
ltp
    test
        ltpdriver.c execute: ./ltpdriver <engine ID> <clientId> <cycles> <greenLen> <adulen>
        include: platform.h/zco.h/ltpP.h
        run_ltpdriver()
            ltp_attach() <library/libltp.c include/ltp.h>
            
    include
        platform.h
        zco.h
    library
        ltpP.h
    
        
        
        

    

ltpdriver.c</ltp/test>:

main -> run_ltp_driver -> 

./ltpdriver <engine ID> <clientId> <cycles> <greenLen> <adulen>
./ltpdriver 10 2 3 100 100

destEngineId == 0 || clientId < 1 || cyclesRemaining < 1 || greenLength < 0 || sduLength < 1
will break

```

Burleigh, S., Ramadas, M., and S. Farrell,"Licklider            Transmission Protocol - Motivation", RFC 5325, September            2008.

Farrell, S., Ramadas, M., and S. Burleigh, "Licklider            Transmission Protocol - Security Extensions", RFC 5327,            September 2008.
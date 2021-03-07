```bash
export LD_LIBRARY_PATH=/home/lht/mini_ltp/ltp/i86-redhat/lib"

sudo cp ../lib/libltp.so /usr/lib
sudo cp ../lib/libici.so /usr/lib

./ltp/i86-redhat/bin/ltpadmin
```

```
ltp
    test
        ltpdriver.c execute: ./ltpdriver <engine ID> <clientId> <cycles> <greenLen> <adulen>
        include: platform.h/zco.h/ltpP.h
        run_ltpdriver()
            ltp_attach() <library/libltp.c include/ltp.h>
        
        ➜  bin git:(master) ✗ ./ltpdriver 10 10 1 0 7 
        at line 59 of library/platform_sm.c, Can't get shared memory segment: Invalid argument (0)
        at line 286 of library/memmgr.c, Can't open memory region.
        at line 342 of sdr/sdrxn.c, Can't open SDR working memory.
        at line 483 of sdr/sdrxn.c, Can't open SDR working memory.
        at line 611 of library/ion.c, Can't initialize the SDR system.
        at line 1061 of ../library/libltpP.c, LTP can't attach to ION.
        at line 54 of ../test/ltpdriver.c, ltpdriver can't initialize LTP.

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
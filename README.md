# procstat
displays linux proc stat (/proc/pid/stat) in human-readable format

# summary
Small tool to translate cryptic info from /proc/[pid]/stat
into understandable form. Actually, ps shows most of things
needed. But this will show you everything at once in mostly
raw format.

Read man 5 proc about meaning of fields. 

Without arguments procstat reads stat info from stdin.

# example
```
./procstat $(pidof bash)
                 pid: 5054
               tcomm: (bash)
               state: S
                ppid: 3037
                pgid: 5054
                 sid: 5054
              tty_nr: 34837
            tty_pgrp: 5504
               flags: 4194304
             min_flt: 8400
            cmin_flt: 200357
             maj_flt: 0
            cmaj_flt: 44
               utime: 0.410000
               stime: 0.140000
              cutime: 6.700000
              cstime: 0.960000
            priority: 20
                nice: 0
         num_threads: 1
       it_real_value: 0.000000
          start_time: 08.14 21:35 (1236.27s)
               vsize: 24473600
                 rss: 1729
              rsslim: 9223372036854775807
          start_code: 4194304
            end_code: 5192876
         start_stack: 140736035846880
                 esp: 140736035845544
                 eip: 140393689751674
             pending: 0000000000000000
             blocked: 0000000000010000
              sigign: 0000000000380004
            sigcatch: 000000004b817efb
               wchan: 1
               zero1: 0
               zero2: 0
         exit_signal: 0000000000000011
                 cpu: 0
         rt_priority: 0
              policy: SCHED_OTHER
```

# thanks

http://brokestream.com/procstat.html 

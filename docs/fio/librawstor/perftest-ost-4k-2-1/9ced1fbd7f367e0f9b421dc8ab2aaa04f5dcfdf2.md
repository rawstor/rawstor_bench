[&lt; back](..)

# perftest-ost-4k-2-1

2026-11-17 21:13:26

refs/heads/worktree-ref-tenant-to-account

[9ced1fb](https://github.com/rawstor/librawstor/commit/9ced1fbd7f367e0f9b421dc8ab2aaa04f5dcfdf2)

rw = randread, bs = 4k, iodepth = 2, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=16204: Tue Nov 17 21:09:01 2026
  read: IOPS=54.7k, BW=214MiB/s (224MB/s)(2137MiB/10001msec)
    slat (nsec): min=381, max=56464, avg=1498.62, stdev=588.16
    clat (usec): min=22, max=231, avg=34.77, stdev= 7.25
     lat (usec): min=23, max=247, avg=36.27, stdev= 7.42
    clat percentiles (usec):
     |  1.00th=[   24],  5.00th=[   24], 10.00th=[   25], 20.00th=[   30],
     | 30.00th=[   33], 40.00th=[   34], 50.00th=[   35], 60.00th=[   36],
     | 70.00th=[   38], 80.00th=[   39], 90.00th=[   43], 95.00th=[   49],
     | 99.00th=[   59], 99.50th=[   62], 99.90th=[   72], 99.95th=[   78],
     | 99.99th=[  114]
   bw (  KiB/s): min=171695, max=229512, per=100.00%, avg=218936.55, stdev=17377.33, samples=20
   iops        : min=42923, max=57378, avg=54734.15, stdev=4344.45, samples=20
  lat (usec)   : 50=95.89%, 100=4.09%, 250=0.01%
  cpu          : usr=33.40%, sys=51.42%, ctx=226251, majf=0, minf=36
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=547078,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2
randwrite: (groupid=1, jobs=1): err= 0: pid=16208: Tue Nov 17 21:09:01 2026
  write: IOPS=2114, BW=8460KiB/s (8663kB/s)(83.8MiB/10145msec); 0 zone resets
    slat (nsec): min=711, max=52157, avg=6287.16, stdev=2008.27
    clat (usec): min=247, max=414807, avg=941.35, stdev=8196.20
     lat (usec): min=252, max=414813, avg=947.64, stdev=8196.22
    clat percentiles (usec):
     |  1.00th=[   281],  5.00th=[   302], 10.00th=[   318], 20.00th=[   343],
     | 30.00th=[   363], 40.00th=[   375], 50.00th=[   392], 60.00th=[   412],
     | 70.00th=[   445], 80.00th=[   515], 90.00th=[   627], 95.00th=[   840],
     | 99.00th=[  3982], 99.50th=[ 16581], 99.90th=[137364], 99.95th=[193987],
     | 99.99th=[252707]
   bw (  KiB/s): min= 2344, max=17304, per=100.00%, avg=8585.05, stdev=4401.22, samples=20
   iops        : min=  586, max= 4326, avg=2146.25, stdev=1100.31, samples=20
  lat (usec)   : 250=0.01%, 500=78.42%, 750=15.38%, 1000=2.61%
  lat (msec)   : 2=2.10%, 4=0.48%, 10=0.34%, 20=0.21%, 50=0.11%
  lat (msec)   : 100=0.21%, 250=0.11%, 500=0.02%
  cpu          : usr=3.50%, sys=4.49%, ctx=20164, majf=0, minf=36
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,21456,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=214MiB/s (224MB/s), 214MiB/s-214MiB/s (224MB/s-224MB/s), io=2137MiB (2241MB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=8460KiB/s (8663kB/s), 8460KiB/s-8460KiB/s (8663kB/s-8663kB/s), io=83.8MiB (87.9MB), run=10145-10145msec

Disk stats (read/write):
  nvme0n1: ios=1/55111, sectors=8/1266032, merge=0/82200, ticks=0/25884, in_queue=25886, util=41.25%
```

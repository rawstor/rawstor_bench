[&lt; back](..)

# perftest--without-liburing-ost-4k-1-1

2026-11-16 21:04:41

refs/heads/add/security-authorization

[bad7dc5](https://github.com/rawstor/librawstor/commit/bad7dc5e9daf991dedda6e426d6eb5ed774ca05d)

rw = randread, bs = 4k, iodepth = 1, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=16400: Mon Nov 16 21:04:17 2026
  read: IOPS=10.1k, BW=39.4MiB/s (41.3MB/s)(394MiB/10001msec)
    slat (nsec): min=3236, max=38231, avg=4217.58, stdev=1459.18
    clat (usec): min=73, max=326, avg=93.69, stdev=14.18
     lat (usec): min=77, max=331, avg=97.91, stdev=14.63
    clat percentiles (usec):
     |  1.00th=[   77],  5.00th=[   79], 10.00th=[   80], 20.00th=[   82],
     | 30.00th=[   83], 40.00th=[   85], 50.00th=[   88], 60.00th=[   98],
     | 70.00th=[  104], 80.00th=[  106], 90.00th=[  112], 95.00th=[  119],
     | 99.00th=[  135], 99.50th=[  137], 99.90th=[  147], 99.95th=[  153],
     | 99.99th=[  172]
   bw (  KiB/s): min=36392, max=44152, per=100.00%, avg=40339.00, stdev=2230.26, samples=20
   iops        : min= 9098, max=11038, avg=10084.70, stdev=557.57, samples=20
  lat (usec)   : 100=61.84%, 250=38.16%, 500=0.01%
  cpu          : usr=19.59%, sys=24.90%, ctx=100810, majf=0, minf=37
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=100805,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1
randwrite: (groupid=1, jobs=1): err= 0: pid=16404: Mon Nov 16 21:04:17 2026
  write: IOPS=2039, BW=8158KiB/s (8354kB/s)(79.7MiB/10001msec); 0 zone resets
    slat (nsec): min=7614, max=41408, avg=9976.05, stdev=2548.89
    clat (usec): min=330, max=5831, avg=478.45, stdev=241.55
     lat (usec): min=338, max=5842, avg=488.43, stdev=241.58
    clat percentiles (usec):
     |  1.00th=[  355],  5.00th=[  367], 10.00th=[  379], 20.00th=[  404],
     | 30.00th=[  420], 40.00th=[  433], 50.00th=[  445], 60.00th=[  457],
     | 70.00th=[  469], 80.00th=[  490], 90.00th=[  529], 95.00th=[  603],
     | 99.00th=[ 1549], 99.50th=[ 2409], 99.90th=[ 3326], 99.95th=[ 4146],
     | 99.99th=[ 5342]
   bw (  KiB/s): min= 7600, max= 8496, per=100.00%, avg=8161.95, stdev=271.64, samples=20
   iops        : min= 1900, max= 2124, avg=2040.45, stdev=67.94, samples=20
  lat (usec)   : 500=83.41%, 750=13.99%, 1000=1.01%
  lat (msec)   : 2=0.89%, 4=0.64%, 10=0.06%
  cpu          : usr=5.99%, sys=5.73%, ctx=20401, majf=0, minf=37
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,20398,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=39.4MiB/s (41.3MB/s), 39.4MiB/s-39.4MiB/s (41.3MB/s-41.3MB/s), io=394MiB (413MB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=8158KiB/s (8354kB/s), 8158KiB/s-8158KiB/s (8354kB/s-8354kB/s), io=79.7MiB (83.6MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=1/51698, sectors=8/1226728, merge=0/78320, ticks=5/7900, in_queue=7906, util=29.22%
```

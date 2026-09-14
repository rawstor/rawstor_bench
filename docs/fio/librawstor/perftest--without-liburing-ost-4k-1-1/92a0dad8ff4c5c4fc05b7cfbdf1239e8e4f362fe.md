[&lt; back](..)

# perftest--without-liburing-ost-4k-1-1

2026-09-14 09:59:18

refs/heads/releases/v0.2.11

[92a0dad](https://github.com/rawstor/librawstor/commit/92a0dad8ff4c5c4fc05b7cfbdf1239e8e4f362fe)

rw = randread, bs = 4k, iodepth = 1, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=14035: Mon Sep 14 09:58:47 2026
  read: IOPS=10.3k, BW=40.2MiB/s (42.2MB/s)(402MiB/10001msec)
    slat (nsec): min=590, max=21861, avg=951.44, stdev=196.11
    clat (usec): min=62, max=209, avg=95.00, stdev=10.90
     lat (usec): min=63, max=210, avg=95.96, stdev=11.03
    clat percentiles (usec):
     |  1.00th=[   80],  5.00th=[   83], 10.00th=[   84], 20.00th=[   85],
     | 30.00th=[   87], 40.00th=[   88], 50.00th=[   90], 60.00th=[  101],
     | 70.00th=[  105], 80.00th=[  106], 90.00th=[  109], 95.00th=[  111],
     | 99.00th=[  121], 99.50th=[  126], 99.90th=[  137], 99.95th=[  143],
     | 99.99th=[  163]
   bw (  KiB/s): min=37224, max=45400, per=100.00%, avg=41225.20, stdev=2511.27, samples=20
   iops        : min= 9306, max=11350, avg=10306.20, stdev=627.79, samples=20
  lat (usec)   : 100=58.14%, 250=41.86%
  cpu          : usr=14.04%, sys=28.16%, ctx=103036, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=103026,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1
randwrite: (groupid=1, jobs=1): err= 0: pid=14038: Mon Sep 14 09:58:47 2026
  write: IOPS=5609, BW=21.9MiB/s (23.0MB/s)(219MiB/10001msec); 0 zone resets
    slat (nsec): min=1563, max=47819, avg=2113.84, stdev=952.11
    clat (usec): min=146, max=2247, avg=174.69, stdev=19.63
     lat (usec): min=147, max=2250, avg=176.81, stdev=19.78
    clat percentiles (usec):
     |  1.00th=[  153],  5.00th=[  155], 10.00th=[  157], 20.00th=[  157],
     | 30.00th=[  161], 40.00th=[  172], 50.00th=[  180], 60.00th=[  182],
     | 70.00th=[  184], 80.00th=[  186], 90.00th=[  194], 95.00th=[  198],
     | 99.00th=[  208], 99.50th=[  215], 99.90th=[  233], 99.95th=[  245],
     | 99.99th=[  306]
   bw (  KiB/s): min=    8, max=24513, per=95.28%, avg=21378.29, stdev=4975.37, samples=21
   iops        : min=    2, max= 6128, avg=5344.52, stdev=1243.83, samples=21
  lat (usec)   : 250=99.96%, 500=0.03%, 1000=0.01%
  lat (msec)   : 4=0.01%
  cpu          : usr=11.91%, sys=53.29%, ctx=56211, majf=0, minf=1795268
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,56101,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=40.2MiB/s (42.2MB/s), 40.2MiB/s-40.2MiB/s (42.2MB/s-42.2MB/s), io=402MiB (422MB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=21.9MiB/s (23.0MB/s), 21.9MiB/s-21.9MiB/s (23.0MB/s-23.0MB/s), io=219MiB (230MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=0/425, sectors=0/325752, merge=0/935, ticks=0/709, in_queue=709, util=0.16%
```

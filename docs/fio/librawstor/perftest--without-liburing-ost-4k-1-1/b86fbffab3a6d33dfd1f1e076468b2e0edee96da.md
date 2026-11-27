[&lt; back](..)

# perftest--without-liburing-ost-4k-1-1

2026-11-27 08:20:04

refs/heads/add/ost-registration

[b86fbff](https://github.com/rawstor/librawstor/commit/b86fbffab3a6d33dfd1f1e076468b2e0edee96da)

rw = randread, bs = 4k, iodepth = 1, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=16894: Fri Nov 27 08:19:16 2026
  read: IOPS=14.3k, BW=55.8MiB/s (58.5MB/s)(558MiB/10001msec)
    slat (usec): min=2, max=1571, avg= 3.32, stdev= 6.20
    clat (usec): min=41, max=3792, avg=65.89, stdev=26.41
     lat (usec): min=44, max=3804, avg=69.21, stdev=27.87
    clat percentiles (usec):
     |  1.00th=[   52],  5.00th=[   53], 10.00th=[   54], 20.00th=[   55],
     | 30.00th=[   57], 40.00th=[   59], 50.00th=[   61], 60.00th=[   67],
     | 70.00th=[   72], 80.00th=[   76], 90.00th=[   83], 95.00th=[   89],
     | 99.00th=[  108], 99.50th=[  122], 99.90th=[  269], 99.95th=[  445],
     | 99.99th=[  938]
   bw (  KiB/s): min=47664, max=63816, per=100.00%, avg=57160.85, stdev=3868.62, samples=20
   iops        : min=11916, max=15954, avg=14290.15, stdev=967.15, samples=20
  lat (usec)   : 50=0.01%, 100=98.30%, 250=1.59%, 500=0.07%, 750=0.02%
  lat (usec)   : 1000=0.01%
  lat (msec)   : 2=0.01%, 4=0.01%
  cpu          : usr=20.81%, sys=20.25%, ctx=142843, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=142844,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1
randwrite: (groupid=1, jobs=1): err= 0: pid=16896: Fri Nov 27 08:19:16 2026
  write: IOPS=2355, BW=9422KiB/s (9648kB/s)(92.0MiB/10001msec); 0 zone resets
    slat (usec): min=4, max=1437, avg= 7.43, stdev=12.01
    clat (usec): min=254, max=8626, avg=415.64, stdev=201.69
     lat (usec): min=260, max=8636, avg=423.06, stdev=202.42
    clat percentiles (usec):
     |  1.00th=[  281],  5.00th=[  302], 10.00th=[  314], 20.00th=[  338],
     | 30.00th=[  363], 40.00th=[  379], 50.00th=[  392], 60.00th=[  408],
     | 70.00th=[  424], 80.00th=[  449], 90.00th=[  494], 95.00th=[  553],
     | 99.00th=[ 1012], 99.50th=[ 1336], 99.90th=[ 3032], 99.95th=[ 4146],
     | 99.99th=[ 6915]
   bw (  KiB/s): min= 8336, max=10296, per=100.00%, avg=9426.50, stdev=503.68, samples=20
   iops        : min= 2084, max= 2574, avg=2356.45, stdev=125.91, samples=20
  lat (usec)   : 500=90.75%, 750=7.34%, 1000=0.91%
  lat (msec)   : 2=0.72%, 4=0.22%, 10=0.06%
  cpu          : usr=5.23%, sys=4.56%, ctx=23561, majf=0, minf=37
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,23557,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=55.8MiB/s (58.5MB/s), 55.8MiB/s-55.8MiB/s (58.5MB/s-58.5MB/s), io=558MiB (585MB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=9422KiB/s (9648kB/s), 9422KiB/s-9422KiB/s (9648kB/s-9648kB/s), io=92.0MiB (96.5MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=2/58079, sectors=16/1358912, merge=0/87964, ticks=4/7604, in_queue=7607, util=28.83%
```

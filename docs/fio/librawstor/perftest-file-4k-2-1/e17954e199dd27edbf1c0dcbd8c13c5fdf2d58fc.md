[&lt; back](..)

# perftest-file-4k-2-1

2026-11-20 11:26:39

refs/heads/main

[e17954e](https://github.com/rawstor/librawstor/commit/e17954e199dd27edbf1c0dcbd8c13c5fdf2d58fc)

rw = randread, bs = 4k, iodepth = 2, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=16555: Fri Nov 20 11:26:01 2026
  read: IOPS=566k, BW=2211MiB/s (2318MB/s)(21.6GiB/10001msec)
    slat (nsec): min=232, max=32873, avg=288.46, stdev=185.75
    clat (nsec): min=2296, max=99221, avg=3060.93, stdev=652.04
     lat (nsec): min=2579, max=99507, avg=3349.39, stdev=688.00
    clat percentiles (nsec):
     |  1.00th=[ 2704],  5.00th=[ 2800], 10.00th=[ 2832], 20.00th=[ 2896],
     | 30.00th=[ 2928], 40.00th=[ 2960], 50.00th=[ 3024], 60.00th=[ 3056],
     | 70.00th=[ 3088], 80.00th=[ 3152], 90.00th=[ 3216], 95.00th=[ 3312],
     | 99.00th=[ 3824], 99.50th=[ 4448], 99.90th=[13120], 99.95th=[14912],
     | 99.99th=[18560]
   bw (  MiB/s): min= 2175, max= 2239, per=100.00%, avg=2212.33, stdev=19.01, samples=20
   iops        : min=556964, max=573234, avg=566356.90, stdev=4867.82, samples=20
  lat (usec)   : 4=99.20%, 10=0.47%, 20=0.33%, 50=0.01%, 100=0.01%
  cpu          : usr=42.23%, sys=57.75%, ctx=59, majf=0, minf=36
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=5660416,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2
randwrite: (groupid=1, jobs=1): err= 0: pid=16560: Fri Nov 20 11:26:01 2026
  write: IOPS=3144, BW=12.3MiB/s (12.9MB/s)(123MiB/10001msec); 0 zone resets
    slat (nsec): min=569, max=31403, avg=2217.05, stdev=2028.51
    clat (usec): min=285, max=109850, avg=632.24, stdev=1506.50
     lat (usec): min=287, max=109851, avg=634.45, stdev=1506.62
    clat percentiles (usec):
     |  1.00th=[  367],  5.00th=[  400], 10.00th=[  420], 20.00th=[  457],
     | 30.00th=[  490], 40.00th=[  537], 50.00th=[  578], 60.00th=[  611],
     | 70.00th=[  644], 80.00th=[  709], 90.00th=[  840], 95.00th=[  930],
     | 99.00th=[ 1106], 99.50th=[ 1172], 99.90th=[ 1565], 99.95th=[18482],
     | 99.99th=[88605]
   bw (  KiB/s): min= 5635, max=13760, per=100.00%, avg=12583.70, stdev=2184.48, samples=20
   iops        : min= 1408, max= 3440, avg=3145.80, stdev=546.21, samples=20
  lat (usec)   : 500=32.37%, 750=50.49%, 1000=14.47%
  lat (msec)   : 2=2.58%, 4=0.02%, 10=0.02%, 20=0.02%, 50=0.01%
  lat (msec)   : 100=0.03%, 250=0.01%
  cpu          : usr=2.88%, sys=2.13%, ctx=32817, majf=0, minf=36
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,31447,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=2211MiB/s (2318MB/s), 2211MiB/s-2211MiB/s (2318MB/s-2318MB/s), io=21.6GiB (23.2GB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=12.3MiB/s (12.9MB/s), 12.3MiB/s-12.3MiB/s (12.9MB/s-12.9MB/s), io=123MiB (129MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=2/76981, sectors=16/2125656, merge=0/113189, ticks=54/143310, in_queue=143370, util=43.78%
```

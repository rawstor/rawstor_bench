[&lt; back](..)

# perftest-file-4k-2-1

2026-11-23 13:30:22

refs/heads/fix/drop-server-error-log-v0.3

[d618cec](https://github.com/rawstor/librawstor/commit/d618cec76b6f4d37dc9c6a8cb6a3a270c0fefafe)

rw = randread, bs = 4k, iodepth = 2, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=16432: Mon Nov 23 13:28:02 2026
  read: IOPS=599k, BW=2338MiB/s (2452MB/s)(22.8GiB/10001msec)
    slat (nsec): min=150, max=194123, avg=200.38, stdev=302.87
    clat (usec): min=2, max=334, avg= 3.01, stdev= 1.34
     lat (usec): min=2, max=334, avg= 3.21, stdev= 1.37
    clat percentiles (nsec):
     |  1.00th=[ 2640],  5.00th=[ 2704], 10.00th=[ 2768], 20.00th=[ 2800],
     | 30.00th=[ 2864], 40.00th=[ 2896], 50.00th=[ 2960], 60.00th=[ 2992],
     | 70.00th=[ 3056], 80.00th=[ 3120], 90.00th=[ 3184], 95.00th=[ 3280],
     | 99.00th=[ 3792], 99.50th=[ 4256], 99.90th=[10816], 99.95th=[12480],
     | 99.99th=[78336]
   bw (  MiB/s): min= 2179, max= 2405, per=100.00%, avg=2339.58, stdev=50.42, samples=20
   iops        : min=557904, max=615897, avg=598932.20, stdev=12907.29, samples=20
  lat (usec)   : 4=99.27%, 10=0.42%, 20=0.29%, 50=0.01%, 100=0.01%
  lat (usec)   : 250=0.01%, 500=0.01%
  cpu          : usr=33.50%, sys=66.48%, ctx=70, majf=0, minf=36
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=5986494,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2
randwrite: (groupid=1, jobs=1): err= 0: pid=16437: Mon Nov 23 13:28:02 2026
  write: IOPS=5103, BW=19.9MiB/s (20.9MB/s)(199MiB/10001msec); 0 zone resets
    slat (nsec): min=320, max=17216, avg=666.48, stdev=415.14
    clat (usec): min=208, max=112680, avg=390.83, stdev=974.07
     lat (usec): min=208, max=112682, avg=391.50, stdev=974.11
    clat percentiles (usec):
     |  1.00th=[  233],  5.00th=[  247], 10.00th=[  260], 20.00th=[  281],
     | 30.00th=[  297], 40.00th=[  310], 50.00th=[  330], 60.00th=[  359],
     | 70.00th=[  392], 80.00th=[  441], 90.00th=[  537], 95.00th=[  611],
     | 99.00th=[  922], 99.50th=[ 1123], 99.90th=[ 2180], 99.95th=[ 9634],
     | 99.99th=[49021]
   bw (  KiB/s): min= 7808, max=22496, per=100.00%, avg=20424.55, stdev=3407.31, samples=20
   iops        : min= 1952, max= 5624, avg=5106.00, stdev=851.86, samples=20
  lat (usec)   : 250=5.95%, 500=80.24%, 750=11.81%, 1000=1.24%
  lat (msec)   : 2=0.65%, 4=0.05%, 10=0.01%, 20=0.02%, 50=0.02%
  lat (msec)   : 100=0.01%, 250=0.01%
  cpu          : usr=1.12%, sys=3.30%, ctx=56639, majf=0, minf=36
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,51042,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=2338MiB/s (2452MB/s), 2338MiB/s-2338MiB/s (2452MB/s-2452MB/s), io=22.8GiB (24.5GB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=19.9MiB/s (20.9MB/s), 19.9MiB/s-19.9MiB/s (20.9MB/s-20.9MB/s), io=199MiB (209MB), run=10001-10001msec

Disk stats (read/write):
  nvme0n1: ios=2/119426, sectors=16/3170992, merge=0/185238, ticks=10/88475, in_queue=88488, util=43.34%
```

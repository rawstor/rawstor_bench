[&lt; back](..)

# perftest-file-4k-2-1

2026-11-20 10:30:46

refs/heads/add/list-by-location

[a23f3a5](https://github.com/rawstor/librawstor/commit/a23f3a5bf1aec5777cdd731d4bfbfe89e85fdd79)

rw = randread, bs = 4k, iodepth = 2, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=16307: Fri Nov 20 10:29:10 2026
  read: IOPS=624k, BW=2439MiB/s (2557MB/s)(23.8GiB/10001msec)
    slat (nsec): min=140, max=242647, avg=194.08, stdev=229.90
    clat (nsec): min=2263, max=254394, avg=2883.68, stdev=943.69
     lat (nsec): min=2474, max=288866, avg=3077.76, stdev=973.93
    clat percentiles (nsec):
     |  1.00th=[ 2512],  5.00th=[ 2576], 10.00th=[ 2640], 20.00th=[ 2672],
     | 30.00th=[ 2736], 40.00th=[ 2768], 50.00th=[ 2832], 60.00th=[ 2864],
     | 70.00th=[ 2928], 80.00th=[ 2992], 90.00th=[ 3120], 95.00th=[ 3216],
     | 99.00th=[ 3504], 99.50th=[ 3984], 99.90th=[10048], 99.95th=[11840],
     | 99.99th=[29568]
   bw (  MiB/s): min= 2276, max= 2553, per=100.00%, avg=2439.94, stdev=73.22, samples=20
   iops        : min=582758, max=653739, avg=624624.20, stdev=18744.50, samples=20
  lat (usec)   : 4=99.50%, 10=0.38%, 20=0.10%, 50=0.01%, 100=0.01%
  lat (usec)   : 250=0.01%, 500=0.01%
  cpu          : usr=33.71%, sys=66.27%, ctx=55, majf=0, minf=36
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=6243316,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2
randwrite: (groupid=1, jobs=1): err= 0: pid=16314: Fri Nov 20 10:29:10 2026
  write: IOPS=4460, BW=17.4MiB/s (18.3MB/s)(174MiB/10001msec); 0 zone resets
    slat (nsec): min=290, max=13140, avg=630.04, stdev=357.81
    clat (usec): min=207, max=108837, avg=447.37, stdev=1246.07
     lat (usec): min=207, max=108838, avg=448.00, stdev=1246.13
    clat percentiles (usec):
     |  1.00th=[  231],  5.00th=[  245], 10.00th=[  258], 20.00th=[  277],
     | 30.00th=[  293], 40.00th=[  310], 50.00th=[  334], 60.00th=[  363],
     | 70.00th=[  392], 80.00th=[  441], 90.00th=[  537], 95.00th=[  619],
     | 99.00th=[ 2868], 99.50th=[ 5473], 99.90th=[12387], 99.95th=[14615],
     | 99.99th=[53740]
   bw (  KiB/s): min= 7952, max=22488, per=100.00%, avg=17851.95, stdev=3616.69, samples=20
   iops        : min= 1988, max= 5622, avg=4462.95, stdev=904.16, samples=20
  lat (usec)   : 250=7.03%, 500=79.32%, 750=11.06%, 1000=0.56%
  lat (msec)   : 2=0.74%, 4=0.56%, 10=0.62%, 20=0.07%, 50=0.02%
  lat (msec)   : 100=0.01%, 250=0.01%
  cpu          : usr=0.86%, sys=2.73%, ctx=49123, majf=0, minf=36
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,44613,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=2439MiB/s (2557MB/s), 2439MiB/s-2439MiB/s (2557MB/s-2557MB/s), io=23.8GiB (25.6GB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=17.4MiB/s (18.3MB/s), 17.4MiB/s-17.4MiB/s (18.3MB/s-18.3MB/s), io=174MiB (183MB), run=10001-10001msec

Disk stats (read/write):
  nvme0n1: ios=2/104846, sectors=32/3034800, merge=0/162263, ticks=12/98070, in_queue=98087, util=46.74%
```

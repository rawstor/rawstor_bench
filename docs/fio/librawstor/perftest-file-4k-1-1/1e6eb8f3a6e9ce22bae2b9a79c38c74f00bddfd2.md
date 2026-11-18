[&lt; back](..)

# perftest-file-4k-1-1

2026-11-18 08:46:20

refs/heads/add/object-image-import-export

[1e6eb8f](https://github.com/rawstor/librawstor/commit/1e6eb8f3a6e9ce22bae2b9a79c38c74f00bddfd2)

rw = randread, bs = 4k, iodepth = 1, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=16451: Wed Nov 18 08:45:30 2026
  read: IOPS=362k, BW=1413MiB/s (1482MB/s)(13.8GiB/10001msec)
    slat (nsec): min=300, max=65342, avg=341.56, stdev=215.44
    clat (nsec): min=1803, max=93114, avg=2174.52, stdev=558.53
     lat (nsec): min=2134, max=93455, avg=2516.09, stdev=605.90
    clat percentiles (nsec):
     |  1.00th=[ 1976],  5.00th=[ 2008], 10.00th=[ 2024], 20.00th=[ 2064],
     | 30.00th=[ 2064], 40.00th=[ 2096], 50.00th=[ 2128], 60.00th=[ 2160],
     | 70.00th=[ 2160], 80.00th=[ 2224], 90.00th=[ 2288], 95.00th=[ 2384],
     | 99.00th=[ 2896], 99.50th=[ 3408], 99.90th=[11328], 99.95th=[11840],
     | 99.99th=[19328]
   bw (  MiB/s): min= 1381, max= 1442, per=100.00%, avg=1413.94, stdev=15.46, samples=20
   iops        : min=353626, max=369254, avg=361968.00, stdev=3956.29, samples=20
  lat (usec)   : 2=4.27%, 4=95.41%, 10=0.09%, 20=0.21%, 50=0.01%
  lat (usec)   : 100=0.01%
  cpu          : usr=38.05%, sys=61.93%, ctx=63, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=3617745,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1
randwrite: (groupid=1, jobs=1): err= 0: pid=16457: Wed Nov 18 08:45:30 2026
  write: IOPS=2931, BW=11.5MiB/s (12.0MB/s)(115MiB/10001msec); 0 zone resets
    slat (nsec): min=1092, max=58669, avg=2206.69, stdev=954.79
    clat (usec): min=234, max=15545, avg=337.59, stdev=146.72
     lat (usec): min=236, max=15547, avg=339.80, stdev=146.76
    clat percentiles (usec):
     |  1.00th=[  255],  5.00th=[  269], 10.00th=[  277], 20.00th=[  289],
     | 30.00th=[  306], 40.00th=[  318], 50.00th=[  326], 60.00th=[  334],
     | 70.00th=[  347], 80.00th=[  363], 90.00th=[  392], 95.00th=[  429],
     | 99.00th=[  570], 99.50th=[  709], 99.90th=[ 1516], 99.95th=[ 2311],
     | 99.99th=[ 7373]
   bw (  KiB/s): min=10533, max=12344, per=100.00%, avg=11730.45, stdev=409.12, samples=20
   iops        : min= 2633, max= 3086, avg=2932.50, stdev=102.34, samples=20
  lat (usec)   : 250=0.39%, 500=97.49%, 750=1.67%, 1000=0.17%
  lat (msec)   : 2=0.23%, 4=0.04%, 10=0.01%, 20=0.01%
  cpu          : usr=2.14%, sys=2.80%, ctx=29317, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,29317,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=1413MiB/s (1482MB/s), 1413MiB/s-1413MiB/s (1482MB/s-1482MB/s), io=13.8GiB (14.8GB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=11.5MiB/s (12.0MB/s), 11.5MiB/s-11.5MiB/s (12.0MB/s-12.0MB/s), io=115MiB (120MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=2/75223, sectors=16/2220472, merge=0/114032, ticks=11/13531, in_queue=13541, util=35.77%
```

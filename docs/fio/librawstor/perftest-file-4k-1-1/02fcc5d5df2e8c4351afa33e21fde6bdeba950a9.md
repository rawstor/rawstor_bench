[&lt; back](..)

# perftest-file-4k-1-1

2026-11-19 18:17:11

refs/heads/add/location-list

[02fcc5d](https://github.com/rawstor/librawstor/commit/02fcc5d5df2e8c4351afa33e21fde6bdeba950a9)

rw = randread, bs = 4k, iodepth = 1, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=16518: Thu Nov 19 18:16:14 2026
  read: IOPS=363k, BW=1419MiB/s (1488MB/s)(13.9GiB/10001msec)
    slat (nsec): min=320, max=53119, avg=361.56, stdev=219.39
    clat (nsec): min=1773, max=64219, avg=2137.07, stdev=550.81
     lat (nsec): min=2114, max=64600, avg=2498.63, stdev=600.47
    clat percentiles (nsec):
     |  1.00th=[ 1928],  5.00th=[ 1976], 10.00th=[ 1992], 20.00th=[ 2008],
     | 30.00th=[ 2040], 40.00th=[ 2064], 50.00th=[ 2096], 60.00th=[ 2096],
     | 70.00th=[ 2128], 80.00th=[ 2192], 90.00th=[ 2256], 95.00th=[ 2352],
     | 99.00th=[ 2736], 99.50th=[ 3312], 99.90th=[11456], 99.95th=[12992],
     | 99.99th=[19840]
   bw (  MiB/s): min= 1391, max= 1457, per=100.00%, avg=1420.10, stdev=23.17, samples=20
   iops        : min=356116, max=373098, avg=363546.15, stdev=5931.41, samples=20
  lat (usec)   : 2=14.65%, 4=85.07%, 10=0.07%, 20=0.21%, 50=0.01%
  lat (usec)   : 100=0.01%
  cpu          : usr=38.35%, sys=61.63%, ctx=69, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=3633682,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1
randwrite: (groupid=1, jobs=1): err= 0: pid=16525: Thu Nov 19 18:16:14 2026
  write: IOPS=2920, BW=11.4MiB/s (12.0MB/s)(114MiB/10001msec); 0 zone resets
    slat (nsec): min=1252, max=26930, avg=2484.79, stdev=851.66
    clat (usec): min=210, max=17366, avg=338.42, stdev=187.71
     lat (usec): min=211, max=17369, avg=340.91, stdev=187.73
    clat percentiles (usec):
     |  1.00th=[  245],  5.00th=[  260], 10.00th=[  269], 20.00th=[  281],
     | 30.00th=[  302], 40.00th=[  314], 50.00th=[  322], 60.00th=[  334],
     | 70.00th=[  347], 80.00th=[  363], 90.00th=[  396], 95.00th=[  433],
     | 99.00th=[  611], 99.50th=[  791], 99.90th=[ 2573], 99.95th=[ 2999],
     | 99.99th=[ 7046]
   bw (  KiB/s): min=10917, max=12304, per=100.00%, avg=11688.10, stdev=361.61, samples=20
   iops        : min= 2729, max= 3076, avg=2921.95, stdev=90.47, samples=20
  lat (usec)   : 250=1.82%, 500=95.74%, 750=1.88%, 1000=0.16%
  lat (msec)   : 2=0.22%, 4=0.12%, 10=0.04%, 20=0.01%
  cpu          : usr=2.35%, sys=2.79%, ctx=29211, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,29210,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=1419MiB/s (1488MB/s), 1419MiB/s-1419MiB/s (1488MB/s-1488MB/s), io=13.9GiB (14.9GB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=11.4MiB/s (12.0MB/s), 11.4MiB/s-11.4MiB/s (12.0MB/s-12.0MB/s), io=114MiB (120MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=1/74277, sectors=8/2212784, merge=0/112577, ticks=8/12678, in_queue=12687, util=35.48%
```

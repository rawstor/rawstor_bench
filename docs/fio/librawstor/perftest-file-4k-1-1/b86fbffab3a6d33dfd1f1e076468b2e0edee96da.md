[&lt; back](..)

# perftest-file-4k-1-1

2026-11-27 08:20:04

refs/heads/add/ost-registration

[b86fbff](https://github.com/rawstor/librawstor/commit/b86fbffab3a6d33dfd1f1e076468b2e0edee96da)

rw = randread, bs = 4k, iodepth = 1, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=16677: Fri Nov 27 08:18:29 2026
  read: IOPS=521k, BW=2036MiB/s (2135MB/s)(19.9GiB/10001msec)
    slat (nsec): min=180, max=175622, avg=223.13, stdev=408.81
    clat (nsec): min=1242, max=344643, avg=1538.05, stdev=1164.39
     lat (nsec): min=1452, max=344863, avg=1761.17, stdev=1234.76
    clat percentiles (nsec):
     |  1.00th=[ 1400],  5.00th=[ 1416], 10.00th=[ 1432], 20.00th=[ 1448],
     | 30.00th=[ 1464], 40.00th=[ 1480], 50.00th=[ 1496], 60.00th=[ 1528],
     | 70.00th=[ 1560], 80.00th=[ 1576], 90.00th=[ 1608], 95.00th=[ 1640],
     | 99.00th=[ 1736], 99.50th=[ 1848], 99.90th=[ 8512], 99.95th=[ 8896],
     | 99.99th=[68096]
   bw (  MiB/s): min= 1940, max= 2082, per=100.00%, avg=2036.84, stdev=38.43, samples=20
   iops        : min=496654, max=533210, avg=521431.55, stdev=9837.75, samples=20
  lat (usec)   : 2=99.71%, 4=0.11%, 10=0.15%, 20=0.02%, 50=0.01%
  lat (usec)   : 100=0.01%, 250=0.01%, 500=0.01%
  cpu          : usr=35.94%, sys=64.04%, ctx=64, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=5213274,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1
randwrite: (groupid=1, jobs=1): err= 0: pid=16682: Fri Nov 27 08:18:29 2026
  write: IOPS=3252, BW=12.7MiB/s (13.3MB/s)(127MiB/10001msec); 0 zone resets
    slat (nsec): min=340, max=80440, avg=475.98, stdev=560.28
    clat (usec): min=209, max=8858, avg=306.73, stdev=114.39
     lat (usec): min=210, max=8859, avg=307.21, stdev=114.43
    clat percentiles (usec):
     |  1.00th=[  229],  5.00th=[  241], 10.00th=[  249], 20.00th=[  265],
     | 30.00th=[  277], 40.00th=[  285], 50.00th=[  297], 60.00th=[  306],
     | 70.00th=[  314], 80.00th=[  326], 90.00th=[  343], 95.00th=[  375],
     | 99.00th=[  685], 99.50th=[ 1020], 99.90th=[ 1729], 99.95th=[ 1991],
     | 99.99th=[ 2474]
   bw (  KiB/s): min=11472, max=13752, per=100.00%, avg=13014.45, stdev=629.18, samples=20
   iops        : min= 2868, max= 3438, avg=3253.55, stdev=157.35, samples=20
  lat (usec)   : 250=10.47%, 500=87.73%, 750=0.93%, 1000=0.34%
  lat (msec)   : 2=0.48%, 4=0.04%, 10=0.01%
  cpu          : usr=0.66%, sys=1.62%, ctx=32532, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,32532,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=2036MiB/s (2135MB/s), 2036MiB/s-2036MiB/s (2135MB/s-2135MB/s), io=19.9GiB (21.4GB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=12.7MiB/s (13.3MB/s), 12.7MiB/s-12.7MiB/s (13.3MB/s-13.3MB/s), io=127MiB (133MB), run=10001-10001msec

Disk stats (read/write):
  nvme0n1: ios=1/83874, sectors=8/1878416, merge=0/126215, ticks=4/25582, in_queue=25586, util=40.36%
```

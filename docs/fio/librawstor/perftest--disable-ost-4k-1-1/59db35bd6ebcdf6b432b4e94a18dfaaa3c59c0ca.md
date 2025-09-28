[&lt; back](..)

# perftest--disable-ost-4k-1-1

2025-09-28 19:24:42

refs/heads/add/socket

[59db35b](https://github.com/rawstor/librawstor/commit/59db35bd6ebcdf6b432b4e94a18dfaaa3c59c0ca)

rw = randrw, bs = 4k, iodepth = 1, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=10501: Sun Sep 28 19:24:39 2025
  read: IOPS=32.7k, BW=128MiB/s (134MB/s)(1278MiB/10001msec)
    slat (nsec): min=10, max=18023, avg=40.63, stdev=95.08
    clat (nsec): min=1263, max=115526, avg=3101.18, stdev=2684.24
     lat (nsec): min=1283, max=115566, avg=3141.80, stdev=2690.24
    clat percentiles (nsec):
     |  1.00th=[ 1576],  5.00th=[ 1640], 10.00th=[ 1688], 20.00th=[ 1752],
     | 30.00th=[ 1848], 40.00th=[ 2096], 50.00th=[ 2224], 60.00th=[ 2416],
     | 70.00th=[ 3056], 80.00th=[ 4016], 90.00th=[ 5152], 95.00th=[ 7264],
     | 99.00th=[14400], 99.50th=[18304], 99.90th=[25984], 99.95th=[30592],
     | 99.99th=[67072]
   bw (  KiB/s): min=111864, max=141896, per=99.64%, avg=130435.37, stdev=8273.05, samples=19
   iops        : min=27966, max=35474, avg=32608.84, stdev=2068.26, samples=19
  write: IOPS=32.7k, BW=128MiB/s (134MB/s)(1277MiB/10001msec); 0 zone resets
    slat (nsec): min=29, max=15249, avg=80.71, stdev=122.79
    clat (usec): min=8, max=376, avg=26.54, stdev= 3.66
     lat (usec): min=8, max=376, avg=26.62, stdev= 3.67
    clat percentiles (nsec):
     |  1.00th=[21120],  5.00th=[22400], 10.00th=[22912], 20.00th=[23680],
     | 30.00th=[24704], 40.00th=[25472], 50.00th=[25984], 60.00th=[26752],
     | 70.00th=[27264], 80.00th=[28544], 90.00th=[31104], 95.00th=[32384],
     | 99.00th=[39680], 99.50th=[42752], 99.90th=[48384], 99.95th=[51456],
     | 99.99th=[87552]
   bw (  KiB/s): min=112024, max=139992, per=99.69%, avg=130350.74, stdev=8248.29, samples=19
   iops        : min=28006, max=34998, avg=32587.68, stdev=2062.07, samples=19
  lat (usec)   : 2=17.23%, 4=22.79%, 10=8.84%, 20=1.23%, 50=49.87%
  lat (usec)   : 100=0.04%, 250=0.01%, 500=0.01%
  cpu          : usr=9.10%, sys=39.41%, ctx=326678, majf=0, minf=31
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=327283,326910,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=128MiB/s (134MB/s), 128MiB/s-128MiB/s (134MB/s-134MB/s), io=1278MiB (1341MB), run=10001-10001msec
  WRITE: bw=128MiB/s (134MB/s), 128MiB/s-128MiB/s (134MB/s-134MB/s), io=1277MiB (1339MB), run=10001-10001msec

Disk stats (read/write):
  sdb: ios=0/23, sectors=0/1824, merge=0/32, ticks=0/6, in_queue=6, util=0.03%
```

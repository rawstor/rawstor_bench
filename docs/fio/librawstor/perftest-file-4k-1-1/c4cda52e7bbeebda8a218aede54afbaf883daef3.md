[&lt; back](..)

# perftest-file-4k-1-1

2025-10-19 09:57:15

refs/heads/feat/ci

[c4cda52](https://github.com/rawstor/librawstor/commit/c4cda52e7bbeebda8a218aede54afbaf883daef3)

rw = randrw, bs = 4k, iodepth = 1, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=10678: Sun Oct 19 09:57:11 2025
  read: IOPS=31.3k, BW=122MiB/s (128MB/s)(1221MiB/10001msec)
    slat (nsec): min=9, max=18144, avg=45.12, stdev=90.00
    clat (nsec): min=1362, max=122209, avg=3315.08, stdev=2732.02
     lat (nsec): min=1392, max=122239, avg=3360.21, stdev=2740.48
    clat percentiles (nsec):
     |  1.00th=[ 1656],  5.00th=[ 1752], 10.00th=[ 1800], 20.00th=[ 1880],
     | 30.00th=[ 1992], 40.00th=[ 2320], 50.00th=[ 2416], 60.00th=[ 2576],
     | 70.00th=[ 3216], 80.00th=[ 4256], 90.00th=[ 5600], 95.00th=[ 7648],
     | 99.00th=[15168], 99.50th=[18816], 99.90th=[26496], 99.95th=[31360],
     | 99.99th=[61696]
   bw (  KiB/s): min=107704, max=139520, per=99.44%, avg=124305.26, stdev=11157.83, samples=19
   iops        : min=26926, max=34880, avg=31076.32, stdev=2789.46, samples=19
  write: IOPS=31.2k, BW=122MiB/s (128MB/s)(1220MiB/10001msec); 0 zone resets
    slat (nsec): min=29, max=15609, avg=75.64, stdev=96.86
    clat (usec): min=8, max=876, avg=27.82, stdev= 4.16
     lat (usec): min=9, max=876, avg=27.90, stdev= 4.17
    clat percentiles (nsec):
     |  1.00th=[22144],  5.00th=[23424], 10.00th=[24192], 20.00th=[25216],
     | 30.00th=[25728], 40.00th=[26752], 50.00th=[27264], 60.00th=[28032],
     | 70.00th=[28544], 80.00th=[29312], 90.00th=[32640], 95.00th=[34560],
     | 99.00th=[41216], 99.50th=[44288], 99.90th=[51456], 99.95th=[54528],
     | 99.99th=[83456]
   bw (  KiB/s): min=106800, max=139208, per=99.51%, avg=124294.74, stdev=11208.77, samples=19
   iops        : min=26700, max=34802, avg=31073.68, stdev=2802.19, samples=19
  lat (usec)   : 2=15.10%, 4=23.69%, 10=9.90%, 20=1.20%, 50=50.03%
  lat (usec)   : 100=0.08%, 250=0.01%, 750=0.01%, 1000=0.01%
  cpu          : usr=8.86%, sys=39.18%, ctx=311983, majf=0, minf=23
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=312553,312288,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=122MiB/s (128MB/s), 122MiB/s-122MiB/s (128MB/s-128MB/s), io=1221MiB (1280MB), run=10001-10001msec
  WRITE: bw=122MiB/s (128MB/s), 122MiB/s-122MiB/s (128MB/s-128MB/s), io=1220MiB (1279MB), run=10001-10001msec

Disk stats (read/write):
  sdb: ios=0/65, sectors=0/126064, merge=0/172, ticks=0/956, in_queue=956, util=0.17%
```

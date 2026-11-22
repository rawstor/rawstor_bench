[&lt; back](..)

# perftest-ost-4k-1-1

2026-11-22 13:26:07

refs/heads/releases/v0.3

[fba59c4](https://github.com/rawstor/librawstor/commit/fba59c4e9eafea1009c7fb6fd0dd9076edea69ff)

rw = randread, bs = 4k, iodepth = 1, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=16521: Sun Nov 22 13:25:43 2026
  read: IOPS=27.6k, BW=108MiB/s (113MB/s)(1079MiB/10001msec)
    slat (nsec): min=965, max=29701, avg=1313.33, stdev=722.51
    clat (usec): min=15, max=1125, avg=34.64, stdev=13.57
     lat (usec): min=16, max=1126, avg=35.96, stdev=13.63
    clat percentiles (usec):
     |  1.00th=[   16],  5.00th=[   17], 10.00th=[   17], 20.00th=[   17],
     | 30.00th=[   21], 40.00th=[   41], 50.00th=[   42], 60.00th=[   42],
     | 70.00th=[   43], 80.00th=[   44], 90.00th=[   47], 95.00th=[   51],
     | 99.00th=[   62], 99.50th=[   67], 99.90th=[   75], 99.95th=[   86],
     | 99.99th=[  165]
   bw (  KiB/s): min=88352, max=190216, per=100.00%, avg=110567.00, stdev=22853.14, samples=20
   iops        : min=22088, max=47554, avg=27641.70, stdev=5713.30, samples=20
  lat (usec)   : 20=29.87%, 50=64.94%, 100=5.16%, 250=0.03%, 500=0.01%
  lat (usec)   : 750=0.01%, 1000=0.01%
  lat (msec)   : 2=0.01%
  cpu          : usr=16.87%, sys=28.95%, ctx=276265, majf=0, minf=37
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=276259,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1
randwrite: (groupid=1, jobs=1): err= 0: pid=16525: Sun Nov 22 13:25:43 2026
  write: IOPS=4248, BW=16.6MiB/s (17.4MB/s)(166MiB/10001msec); 0 zone resets
    slat (nsec): min=2024, max=57790, avg=4002.95, stdev=2343.48
    clat (usec): min=156, max=848, avg=230.83, stdev=28.88
     lat (usec): min=160, max=852, avg=234.84, stdev=29.23
    clat percentiles (usec):
     |  1.00th=[  180],  5.00th=[  190], 10.00th=[  198], 20.00th=[  206],
     | 30.00th=[  217], 40.00th=[  225], 50.00th=[  231], 60.00th=[  237],
     | 70.00th=[  243], 80.00th=[  251], 90.00th=[  265], 95.00th=[  273],
     | 99.00th=[  314], 99.50th=[  334], 99.90th=[  445], 99.95th=[  529],
     | 99.99th=[  660]
   bw (  KiB/s): min=16000, max=18100, per=100.00%, avg=17004.10, stdev=567.32, samples=20
   iops        : min= 4000, max= 4525, avg=4250.95, stdev=141.80, samples=20
  lat (usec)   : 250=79.30%, 500=20.64%, 750=0.06%, 1000=0.01%
  cpu          : usr=4.61%, sys=5.80%, ctx=42492, majf=0, minf=37
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,42489,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=108MiB/s (113MB/s), 108MiB/s-108MiB/s (113MB/s-113MB/s), io=1079MiB (1132MB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=16.6MiB/s (17.4MB/s), 16.6MiB/s-16.6MiB/s (17.4MB/s-17.4MB/s), io=166MiB (174MB), run=10001-10001msec

Disk stats (read/write):
    dm-0: ios=0/299271, sectors=0/2394168, merge=0/0, ticks=0/61295, in_queue=61295, util=22.40%, aggrios=0/97193, aggsectors=0/1428872, aggrmerge=0/81415, aggrticks=0/3261, aggrin_queue=3261, aggrutil=19.12%
  nvme0n1: ios=0/0, sectors=0/0, merge=0/0, ticks=0/0, in_queue=0, util=0.00%
  nvme1n1: ios=0/194387, sectors=0/2857744, merge=0/162831, ticks=0/6523, in_queue=6523, util=19.12%
```

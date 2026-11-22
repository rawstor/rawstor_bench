[&lt; back](..)

# perftest-file-4k-2-1

2026-11-22 13:26:06

refs/heads/releases/v0.3

[fba59c4](https://github.com/rawstor/librawstor/commit/fba59c4e9eafea1009c7fb6fd0dd9076edea69ff)

rw = randread, bs = 4k, iodepth = 2, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=17013: Sun Nov 22 13:25:34 2026
  read: IOPS=425k, BW=1662MiB/s (1743MB/s)(16.2GiB/10001msec)
    slat (nsec): min=270, max=49823, avg=325.16, stdev=211.26
    clat (nsec): min=3316, max=92703, avg=4153.30, stdev=794.49
     lat (nsec): min=3637, max=93033, avg=4478.47, stdev=832.54
    clat percentiles (nsec):
     |  1.00th=[ 3760],  5.00th=[ 3824], 10.00th=[ 3888], 20.00th=[ 3952],
     | 30.00th=[ 3984], 40.00th=[ 4016], 50.00th=[ 4080], 60.00th=[ 4128],
     | 70.00th=[ 4128], 80.00th=[ 4256], 90.00th=[ 4320], 95.00th=[ 4448],
     | 99.00th=[ 5792], 99.50th=[ 7264], 99.90th=[14272], 99.95th=[19584],
     | 99.99th=[24448]
   bw (  MiB/s): min= 1605, max= 1682, per=100.00%, avg=1663.04, stdev=15.90, samples=20
   iops        : min=411028, max=430771, avg=425738.60, stdev=4069.55, samples=20
  lat (usec)   : 4=32.77%, 10=66.80%, 20=0.38%, 50=0.05%, 100=0.01%
  cpu          : usr=38.94%, sys=61.04%, ctx=52, majf=0, minf=36
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=4255001,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2
randwrite: (groupid=1, jobs=1): err= 0: pid=17017: Sun Nov 22 13:25:34 2026
  write: IOPS=4665, BW=18.2MiB/s (19.1MB/s)(182MiB/10001msec); 0 zone resets
    slat (nsec): min=521, max=37069, avg=2452.99, stdev=1326.72
    clat (usec): min=245, max=12541, avg=424.74, stdev=210.97
     lat (usec): min=247, max=12542, avg=427.19, stdev=210.89
    clat percentiles (usec):
     |  1.00th=[  273],  5.00th=[  289], 10.00th=[  306], 20.00th=[  330],
     | 30.00th=[  347], 40.00th=[  367], 50.00th=[  388], 60.00th=[  412],
     | 70.00th=[  441], 80.00th=[  490], 90.00th=[  586], 95.00th=[  660],
     | 99.00th=[  824], 99.50th=[  963], 99.90th=[ 2671], 99.95th=[ 5014],
     | 99.99th=[ 6849]
   bw (  KiB/s): min=17864, max=19206, per=100.00%, avg=18673.25, stdev=418.48, samples=20
   iops        : min= 4466, max= 4801, avg=4668.20, stdev=104.61, samples=20
  lat (usec)   : 250=0.02%, 500=81.22%, 750=16.86%, 1000=1.45%
  lat (msec)   : 2=0.32%, 4=0.08%, 10=0.06%, 20=0.01%
  cpu          : usr=3.92%, sys=4.96%, ctx=48882, majf=0, minf=36
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,46664,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=1662MiB/s (1743MB/s), 1662MiB/s-1662MiB/s (1743MB/s-1743MB/s), io=16.2GiB (17.4GB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=18.2MiB/s (19.1MB/s), 18.2MiB/s-18.2MiB/s (19.1MB/s-19.1MB/s), io=182MiB (191MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=3/112186, sectors=24/3025136, merge=0/176056, ticks=18/15183, in_queue=15201, util=33.95%
```

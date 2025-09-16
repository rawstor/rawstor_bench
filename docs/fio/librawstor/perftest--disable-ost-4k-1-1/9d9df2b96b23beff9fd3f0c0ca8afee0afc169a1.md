[&lt; back](..)

# perftest--disable-ost-4k-1-1

2025-09-16 21:09:52

refs/heads/main

[9d9df2b](https://github.com/rawstor/librawstor/commit/9d9df2b96b23beff9fd3f0c0ca8afee0afc169a1)

rw = randrw, bs = 4k, iodepth = 1, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=10400: Tue Sep 16 21:09:50 2025
  read: IOPS=32.0k, BW=125MiB/s (131MB/s)(1251MiB/10000msec)
    slat (nsec): min=9, max=17733, avg=44.60, stdev=87.26
    clat (nsec): min=1242, max=130825, avg=3193.18, stdev=2846.33
     lat (nsec): min=1262, max=130875, avg=3237.78, stdev=2852.60
    clat percentiles (nsec):
     |  1.00th=[ 1560],  5.00th=[ 1640], 10.00th=[ 1688], 20.00th=[ 1752],
     | 30.00th=[ 1880], 40.00th=[ 2096], 50.00th=[ 2192], 60.00th=[ 2416],
     | 70.00th=[ 3184], 80.00th=[ 4192], 90.00th=[ 5472], 95.00th=[ 7648],
     | 99.00th=[15040], 99.50th=[18816], 99.90th=[26752], 99.95th=[31360],
     | 99.99th=[72192]
   bw (  KiB/s): min=109432, max=147576, per=100.00%, avg=128140.80, stdev=10986.89, samples=20
   iops        : min=27358, max=36894, avg=32035.20, stdev=2746.72, samples=20
  write: IOPS=32.0k, BW=125MiB/s (131MB/s)(1251MiB/10000msec); 0 zone resets
    slat (nsec): min=29, max=19456, avg=67.93, stdev=108.32
    clat (usec): min=7, max=696, avg=27.08, stdev= 4.53
     lat (usec): min=7, max=696, avg=27.15, stdev= 4.54
    clat percentiles (nsec):
     |  1.00th=[20864],  5.00th=[22400], 10.00th=[22912], 20.00th=[23936],
     | 30.00th=[24960], 40.00th=[25984], 50.00th=[26496], 60.00th=[27008],
     | 70.00th=[27776], 80.00th=[29568], 90.00th=[32128], 95.00th=[33536],
     | 99.00th=[41216], 99.50th=[44800], 99.90th=[51456], 99.95th=[56064],
     | 99.99th=[93696]
   bw (  KiB/s): min=111264, max=144392, per=100.00%, avg=128065.20, stdev=10660.62, samples=20
   iops        : min=27816, max=36098, avg=32016.30, stdev=2665.19, samples=20
  lat (usec)   : 2=17.08%, 4=22.21%, 10=9.41%, 20=1.37%, 50=49.85%
  lat (usec)   : 100=0.08%, 250=0.01%, 500=0.01%, 750=0.01%
  cpu          : usr=7.95%, sys=39.36%, ctx=319930, majf=0, minf=30
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=320352,320163,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=125MiB/s (131MB/s), 125MiB/s-125MiB/s (131MB/s-131MB/s), io=1251MiB (1312MB), run=10000-10000msec
  WRITE: bw=125MiB/s (131MB/s), 125MiB/s-125MiB/s (131MB/s-131MB/s), io=1251MiB (1311MB), run=10000-10000msec

Disk stats (read/write):
  sdb: ios=0/6, sectors=0/520, merge=0/1, ticks=0/2, in_queue=3, util=0.00%
```

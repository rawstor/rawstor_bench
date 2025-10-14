[&lt; back](..)

# perftest-file-4k-1-1

2025-10-14 20:53:17

refs/heads/test/asan

[3ff1c74](https://github.com/rawstor/librawstor/commit/3ff1c742fe0dfd3a1a5b7ab17cf9baa01f2f678c)

rw = randrw, bs = 4k, iodepth = 1, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=10775: Tue Oct 14 20:53:15 2025
  read: IOPS=32.4k, BW=127MiB/s (133MB/s)(1267MiB/10001msec)
    slat (nsec): min=10, max=14998, avg=44.32, stdev=101.02
    clat (nsec): min=1342, max=113041, avg=3171.83, stdev=2745.40
     lat (nsec): min=1372, max=113081, avg=3216.16, stdev=2752.95
    clat percentiles (nsec):
     |  1.00th=[ 1608],  5.00th=[ 1688], 10.00th=[ 1720], 20.00th=[ 1784],
     | 30.00th=[ 1896], 40.00th=[ 2160], 50.00th=[ 2256], 60.00th=[ 2512],
     | 70.00th=[ 3120], 80.00th=[ 4048], 90.00th=[ 5280], 95.00th=[ 7328],
     | 99.00th=[14912], 99.50th=[18816], 99.90th=[26240], 99.95th=[30336],
     | 99.99th=[73216]
   bw (  KiB/s): min=111184, max=143216, per=99.48%, avg=129014.84, stdev=11476.16, samples=19
   iops        : min=27796, max=35804, avg=32253.68, stdev=2869.08, samples=19
  write: IOPS=32.4k, BW=126MiB/s (133MB/s)(1265MiB/10001msec); 0 zone resets
    slat (nsec): min=50, max=16891, avg=96.25, stdev=133.32
    clat (usec): min=8, max=1108, avg=26.73, stdev= 4.93
     lat (usec): min=8, max=1109, avg=26.82, stdev= 4.94
    clat percentiles (nsec):
     |  1.00th=[20608],  5.00th=[22144], 10.00th=[22656], 20.00th=[23680],
     | 30.00th=[24448], 40.00th=[25472], 50.00th=[25984], 60.00th=[26752],
     | 70.00th=[27520], 80.00th=[29312], 90.00th=[31872], 95.00th=[33536],
     | 99.00th=[40192], 99.50th=[43776], 99.90th=[50432], 99.95th=[55040],
     | 99.99th=[92672]
   bw (  KiB/s): min=112048, max=144576, per=99.54%, avg=128937.37, stdev=11532.63, samples=19
   iops        : min=28012, max=36144, avg=32234.32, stdev=2883.19, samples=19
  lat (usec)   : 2=16.44%, 4=23.38%, 10=8.97%, 20=1.42%, 50=49.72%
  lat (usec)   : 100=0.07%, 250=0.01%, 500=0.01%, 750=0.01%, 1000=0.01%
  lat (msec)   : 2=0.01%
  cpu          : usr=10.05%, sys=38.97%, ctx=323549, majf=0, minf=25
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=324243,323862,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=127MiB/s (133MB/s), 127MiB/s-127MiB/s (133MB/s-133MB/s), io=1267MiB (1328MB), run=10001-10001msec
  WRITE: bw=126MiB/s (133MB/s), 126MiB/s-126MiB/s (133MB/s-133MB/s), io=1265MiB (1327MB), run=10001-10001msec

Disk stats (read/write):
  sdb: ios=0/22, sectors=0/1912, merge=0/36, ticks=0/8, in_queue=8, util=0.01%
```

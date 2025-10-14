[&lt; back](..)

# perftest--without-liburing-file-4k-1-1

2025-10-14 20:53:11

refs/heads/test/asan

[3ff1c74](https://github.com/rawstor/librawstor/commit/3ff1c742fe0dfd3a1a5b7ab17cf9baa01f2f678c)

rw = randrw, bs = 4k, iodepth = 1, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=10832: Tue Oct 14 20:53:09 2025
  read: IOPS=169k, BW=658MiB/s (690MB/s)(6585MiB/10001msec)
    slat (nsec): min=20, max=28423, avg=30.43, stdev=66.91
    clat (nsec): min=1623, max=731552, avg=2342.61, stdev=1381.76
     lat (nsec): min=1652, max=731612, avg=2373.04, stdev=1384.62
    clat percentiles (nsec):
     |  1.00th=[ 1912],  5.00th=[ 1976], 10.00th=[ 2008], 20.00th=[ 2040],
     | 30.00th=[ 2064], 40.00th=[ 2096], 50.00th=[ 2128], 60.00th=[ 2160],
     | 70.00th=[ 2192], 80.00th=[ 2256], 90.00th=[ 2416], 95.00th=[ 3472],
     | 99.00th=[ 7136], 99.50th=[11072], 99.90th=[17280], 99.95th=[20864],
     | 99.99th=[29312]
   bw (  KiB/s): min=356240, max=748760, per=99.59%, avg=671465.68, stdev=122148.19, samples=19
   iops        : min=89060, max=187192, avg=167866.53, stdev=30537.12, samples=19
  write: IOPS=168k, BW=658MiB/s (690MB/s)(6580MiB/10001msec); 0 zone resets
    slat (nsec): min=29, max=23544, avg=43.96, stdev=70.74
    clat (nsec): min=2084, max=98194, avg=2997.27, stdev=1201.77
     lat (nsec): min=2134, max=98234, avg=3041.23, stdev=1205.94
    clat percentiles (nsec):
     |  1.00th=[ 2352],  5.00th=[ 2416], 10.00th=[ 2448], 20.00th=[ 2480],
     | 30.00th=[ 2512], 40.00th=[ 2544], 50.00th=[ 2544], 60.00th=[ 2608],
     | 70.00th=[ 2640], 80.00th=[ 2832], 90.00th=[ 4832], 95.00th=[ 5216],
     | 99.00th=[ 6304], 99.50th=[ 8096], 99.90th=[14144], 99.95th=[16064],
     | 99.99th=[23424]
   bw (  KiB/s): min=356072, max=751064, per=99.57%, avg=670826.53, stdev=122047.27, samples=19
   iops        : min=89018, max=187764, avg=167706.63, stdev=30511.81, samples=19
  lat (usec)   : 2=4.01%, 4=86.53%, 10=8.99%, 20=0.42%, 50=0.03%
  lat (usec)   : 100=0.01%, 250=0.01%, 750=0.01%
  cpu          : usr=28.56%, sys=71.41%, ctx=77, majf=0, minf=39
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=1685787,1684479,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=658MiB/s (690MB/s), 658MiB/s-658MiB/s (690MB/s-690MB/s), io=6585MiB (6905MB), run=10001-10001msec
  WRITE: bw=658MiB/s (690MB/s), 658MiB/s-658MiB/s (690MB/s-690MB/s), io=6580MiB (6900MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=0/23, sectors=0/11056, merge=0/49, ticks=0/21, in_queue=21, util=0.02%
```

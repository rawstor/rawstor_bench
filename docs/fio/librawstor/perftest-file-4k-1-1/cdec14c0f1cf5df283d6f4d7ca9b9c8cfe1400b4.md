[&lt; back](..)

# perftest-file-4k-1-1

2025-10-24 07:14:45

refs/heads/ci/packages

[cdec14c](https://github.com/rawstor/librawstor/commit/cdec14c0f1cf5df283d6f4d7ca9b9c8cfe1400b4)

rw = randrw, bs = 4k, iodepth = 1, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=10906: Fri Oct 24 07:14:43 2025
  read: IOPS=32.0k, BW=125MiB/s (131MB/s)(1250MiB/10001msec)
    slat (nsec): min=10, max=18124, avg=48.51, stdev=102.19
    clat (nsec): min=1393, max=206636, avg=3356.79, stdev=2944.16
     lat (nsec): min=1413, max=206666, avg=3405.30, stdev=2954.86
    clat percentiles (nsec):
     |  1.00th=[ 1688],  5.00th=[ 1784], 10.00th=[ 1848], 20.00th=[ 1912],
     | 30.00th=[ 2040], 40.00th=[ 2224], 50.00th=[ 2320], 60.00th=[ 2608],
     | 70.00th=[ 3344], 80.00th=[ 4256], 90.00th=[ 5664], 95.00th=[ 7776],
     | 99.00th=[15296], 99.50th=[18816], 99.90th=[26496], 99.95th=[30848],
     | 99.99th=[85504]
   bw (  KiB/s): min=104368, max=143584, per=99.38%, avg=127181.05, stdev=13658.40, samples=19
   iops        : min=26092, max=35896, avg=31795.37, stdev=3414.57, samples=19
  write: IOPS=32.0k, BW=125MiB/s (131MB/s)(1249MiB/10001msec); 0 zone resets
    slat (nsec): min=29, max=16100, avg=76.88, stdev=129.73
    clat (usec): min=6, max=498, avg=26.93, stdev= 5.37
     lat (usec): min=7, max=498, avg=27.00, stdev= 5.38
    clat percentiles (usec):
     |  1.00th=[   21],  5.00th=[   22], 10.00th=[   23], 20.00th=[   24],
     | 30.00th=[   25], 40.00th=[   26], 50.00th=[   27], 60.00th=[   27],
     | 70.00th=[   29], 80.00th=[   31], 90.00th=[   33], 95.00th=[   34],
     | 99.00th=[   41], 99.50th=[   45], 99.90th=[   51], 99.95th=[   54],
     | 99.99th=[  128]
   bw (  KiB/s): min=101768, max=143856, per=99.39%, avg=127117.47, stdev=13735.63, samples=19
   iops        : min=25442, max=35964, avg=31779.37, stdev=3433.91, samples=19
  lat (usec)   : 2=14.00%, 4=25.00%, 10=9.64%, 20=1.69%, 50=49.61%
  lat (usec)   : 100=0.06%, 250=0.01%, 500=0.01%
  cpu          : usr=9.92%, sys=38.45%, ctx=319618, majf=0, minf=24
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=319967,319761,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=125MiB/s (131MB/s), 125MiB/s-125MiB/s (131MB/s-131MB/s), io=1250MiB (1311MB), run=10001-10001msec
  WRITE: bw=125MiB/s (131MB/s), 125MiB/s-125MiB/s (131MB/s-131MB/s), io=1249MiB (1310MB), run=10001-10001msec

Disk stats (read/write):
  sdb: ios=0/15, sectors=0/10320, merge=0/63, ticks=0/17, in_queue=17, util=0.02%
```

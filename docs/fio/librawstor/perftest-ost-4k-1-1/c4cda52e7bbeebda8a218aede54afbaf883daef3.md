[&lt; back](..)

# perftest-ost-4k-1-1

2025-10-19 09:57:25

refs/heads/feat/ci

[c4cda52](https://github.com/rawstor/librawstor/commit/c4cda52e7bbeebda8a218aede54afbaf883daef3)

rw = randrw, bs = 4k, iodepth = 1, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=11802: Sun Oct 19 09:57:24 2025
  read: IOPS=5871, BW=22.9MiB/s (24.1MB/s)(229MiB/10001msec)
    slat (nsec): min=30, max=15660, avg=139.34, stdev=143.85
    clat (usec): min=38, max=22575, avg=70.53, stdev=156.00
     lat (usec): min=39, max=22576, avg=70.67, stdev=156.00
    clat percentiles (usec):
     |  1.00th=[   53],  5.00th=[   56], 10.00th=[   58], 20.00th=[   62],
     | 30.00th=[   64], 40.00th=[   67], 50.00th=[   69], 60.00th=[   71],
     | 70.00th=[   74], 80.00th=[   77], 90.00th=[   83], 95.00th=[   89],
     | 99.00th=[  102], 99.50th=[  110], 99.90th=[  131], 99.95th=[  151],
     | 99.99th=[  367]
   bw (  KiB/s): min=21944, max=25112, per=100.00%, avg=23488.80, stdev=991.09, samples=20
   iops        : min= 5486, max= 6278, avg=5872.20, stdev=247.77, samples=20
  write: IOPS=5850, BW=22.9MiB/s (24.0MB/s)(229MiB/10001msec); 0 zone resets
    slat (nsec): min=80, max=18544, avg=232.45, stdev=208.43
    clat (usec): min=57, max=23130, avg=96.65, stdev=203.98
     lat (usec): min=57, max=23131, avg=96.88, stdev=203.98
    clat percentiles (usec):
     |  1.00th=[   75],  5.00th=[   80], 10.00th=[   82], 20.00th=[   86],
     | 30.00th=[   89], 40.00th=[   91], 50.00th=[   94], 60.00th=[   96],
     | 70.00th=[   99], 80.00th=[  102], 90.00th=[  109], 95.00th=[  115],
     | 99.00th=[  129], 99.50th=[  137], 99.90th=[  178], 99.95th=[  225],
     | 99.99th=[ 5604]
   bw (  KiB/s): min=21576, max=26040, per=100.00%, avg=23402.80, stdev=1115.93, samples=20
   iops        : min= 5394, max= 6510, avg=5850.70, stdev=278.98, samples=20
  lat (usec)   : 50=0.17%, 100=86.10%, 250=13.70%, 500=0.01%, 750=0.01%
  lat (msec)   : 2=0.01%, 10=0.01%, 50=0.01%
  cpu          : usr=7.58%, sys=34.30%, ctx=117790, majf=0, minf=42
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=58722,58507,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=22.9MiB/s (24.1MB/s), 22.9MiB/s-22.9MiB/s (24.1MB/s-24.1MB/s), io=229MiB (241MB), run=10001-10001msec
  WRITE: bw=22.9MiB/s (24.0MB/s), 22.9MiB/s-22.9MiB/s (24.0MB/s-24.0MB/s), io=229MiB (240MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=0/300, sectors=0/54424, merge=0/1500, ticks=0/224, in_queue=229, util=0.19%
```

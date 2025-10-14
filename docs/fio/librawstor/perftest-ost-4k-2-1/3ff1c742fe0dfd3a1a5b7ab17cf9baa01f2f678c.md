[&lt; back](..)

# perftest-ost-4k-2-1

2025-10-14 20:53:46

refs/heads/test/asan

[3ff1c74](https://github.com/rawstor/librawstor/commit/3ff1c742fe0dfd3a1a5b7ab17cf9baa01f2f678c)

rw = randrw, bs = 4k, iodepth = 2, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=11760: Tue Oct 14 20:53:44 2025
  read: IOPS=10.7k, BW=41.8MiB/s (43.9MB/s)(419MiB/10015msec)
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=105, max=10118, avg=5117.39, stdev=2903.65
     lat (usec): min=28, max=28984, avg=81.32, stdev=318.87
    clat percentiles (msec):
     |  1.00th=[  207],  5.00th=[  584], 10.00th=[ 1116], 20.00th=[ 2072],
     | 30.00th=[ 3104], 40.00th=[ 4111], 50.00th=[ 5134], 60.00th=[ 6141],
     | 70.00th=[ 7148], 80.00th=[ 8154], 90.00th=[ 9194], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=38424, max=46632, per=100.00%, avg=42889.60, stdev=1947.28, samples=20
   iops        : min= 9606, max=11658, avg=10722.40, stdev=486.82, samples=20
  write: IOPS=10.7k, BW=41.7MiB/s (43.7MB/s)(418MiB/10015msec); 0 zone resets
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=105, max=10093, avg=5121.41, stdev=2907.27
     lat (usec): min=38, max=33705, avg=102.99, stdev=281.40
    clat percentiles (msec):
     |  1.00th=[  203],  5.00th=[  575], 10.00th=[ 1116], 20.00th=[ 2072],
     | 30.00th=[ 3104], 40.00th=[ 4144], 50.00th=[ 5134], 60.00th=[ 6141],
     | 70.00th=[ 7148], 80.00th=[ 8154], 90.00th=[ 9194], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=38664, max=47048, per=100.00%, avg=42785.20, stdev=2046.82, samples=20
   iops        : min= 9666, max=11762, avg=10696.30, stdev=511.70, samples=20
  lat (msec)   : 250=1.50%, 500=2.64%, 750=2.59%, 1000=2.41%, 2000=10.10%
  lat (msec)   : >=2000=80.76%
  cpu          : usr=11.35%, sys=49.60%, ctx=143394, majf=0, minf=44
  IO depths    : 1=0.1%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=107226,106963,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=41.8MiB/s (43.9MB/s), 41.8MiB/s-41.8MiB/s (43.9MB/s-43.9MB/s), io=419MiB (439MB), run=10015-10015msec
  WRITE: bw=41.7MiB/s (43.7MB/s), 41.7MiB/s-41.7MiB/s (43.7MB/s-43.7MB/s), io=418MiB (438MB), run=10015-10015msec

Disk stats (read/write):
  sdb: ios=0/120, sectors=0/50792, merge=0/1117, ticks=0/259, in_queue=271, util=0.25%
```

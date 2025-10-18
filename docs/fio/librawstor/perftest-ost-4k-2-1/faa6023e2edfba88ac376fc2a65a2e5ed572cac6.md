[&lt; back](..)

# perftest-ost-4k-2-1

2025-10-18 20:38:35

refs/heads/test/asan

[faa6023](https://github.com/rawstor/librawstor/commit/faa6023e2edfba88ac376fc2a65a2e5ed572cac6)

rw = randrw, bs = 4k, iodepth = 2, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=11651: Sat Oct 18 20:38:33 2025
  read: IOPS=10.2k, BW=39.8MiB/s (41.7MB/s)(398MiB/10001msec)
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=105, max=10105, avg=5054.01, stdev=2893.51
     lat (usec): min=28, max=30677, avg=84.81, stdev=268.68
    clat percentiles (msec):
     |  1.00th=[  215],  5.00th=[  592], 10.00th=[ 1083], 20.00th=[ 2022],
     | 30.00th=[ 3037], 40.00th=[ 4010], 50.00th=[ 5067], 60.00th=[ 6074],
     | 70.00th=[ 7080], 80.00th=[ 8087], 90.00th=[ 9060], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=36112, max=44864, per=99.91%, avg=40709.89, stdev=1892.87, samples=19
   iops        : min= 9028, max=11216, avg=10177.47, stdev=473.22, samples=19
  write: IOPS=10.2k, BW=39.7MiB/s (41.6MB/s)(397MiB/10001msec); 0 zone resets
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=106, max=10105, avg=5061.49, stdev=2900.19
     lat (usec): min=48, max=32803, avg=108.75, stdev=324.65
    clat percentiles (msec):
     |  1.00th=[  209],  5.00th=[  592], 10.00th=[ 1083], 20.00th=[ 2005],
     | 30.00th=[ 3037], 40.00th=[ 4010], 50.00th=[ 5067], 60.00th=[ 6074],
     | 70.00th=[ 7080], 80.00th=[ 8087], 90.00th=[ 9060], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=37032, max=44512, per=99.91%, avg=40630.74, stdev=1916.85, samples=19
   iops        : min= 9258, max=11128, avg=10157.68, stdev=479.21, samples=19
  lat (msec)   : 250=1.38%, 500=2.62%, 750=2.76%, 1000=2.68%, 2000=10.44%
  lat (msec)   : >=2000=80.11%
  cpu          : usr=10.18%, sys=48.82%, ctx=141089, majf=0, minf=41
  IO depths    : 1=0.1%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=101875,101678,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=39.8MiB/s (41.7MB/s), 39.8MiB/s-39.8MiB/s (41.7MB/s-41.7MB/s), io=398MiB (417MB), run=10001-10001msec
  WRITE: bw=39.7MiB/s (41.6MB/s), 39.7MiB/s-39.7MiB/s (41.6MB/s-41.6MB/s), io=397MiB (416MB), run=10001-10001msec

Disk stats (read/write):
  sdb: ios=0/303, sectors=0/54400, merge=0/1502, ticks=0/287, in_queue=297, util=0.25%
```

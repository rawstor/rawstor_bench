[&lt; back](..)

# perftest--without-liburing-ost-4k-1-1

2026-11-20 10:30:46

refs/heads/add/list-by-location

[a23f3a5](https://github.com/rawstor/librawstor/commit/a23f3a5bf1aec5777cdd731d4bfbfe89e85fdd79)

rw = randread, bs = 4k, iodepth = 1, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=16298: Fri Nov 20 10:29:30 2026
  read: IOPS=24.9k, BW=97.4MiB/s (102MB/s)(974MiB/10001msec)
    slat (nsec): min=931, max=169757, avg=1070.92, stdev=780.14
    clat (usec): min=31, max=1155, avg=38.85, stdev=10.56
     lat (usec): min=32, max=1157, avg=39.92, stdev=10.67
    clat percentiles (usec):
     |  1.00th=[   35],  5.00th=[   35], 10.00th=[   36], 20.00th=[   36],
     | 30.00th=[   37], 40.00th=[   37], 50.00th=[   38], 60.00th=[   39],
     | 70.00th=[   40], 80.00th=[   41], 90.00th=[   43], 95.00th=[   47],
     | 99.00th=[   56], 99.50th=[   59], 99.90th=[  192], 99.95th=[  269],
     | 99.99th=[  429]
   bw (  KiB/s): min=82008, max=106552, per=100.00%, avg=99749.65, stdev=5674.86, samples=20
   iops        : min=20502, max=26638, avg=24937.30, stdev=1418.68, samples=20
  lat (usec)   : 50=97.39%, 100=2.43%, 250=0.12%, 500=0.05%, 750=0.01%
  lat (usec)   : 1000=0.01%
  lat (msec)   : 2=0.01%
  cpu          : usr=14.57%, sys=29.53%, ctx=249272, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=249266,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1
randwrite: (groupid=1, jobs=1): err= 0: pid=16301: Fri Nov 20 10:29:30 2026
  write: IOPS=2772, BW=10.8MiB/s (11.4MB/s)(108MiB/10001msec); 0 zone resets
    slat (nsec): min=1993, max=116957, avg=2685.31, stdev=1771.00
    clat (usec): min=241, max=15273, avg=357.60, stdev=274.49
     lat (usec): min=243, max=15275, avg=360.28, stdev=274.60
    clat percentiles (usec):
     |  1.00th=[  265],  5.00th=[  281], 10.00th=[  289], 20.00th=[  306],
     | 30.00th=[  318], 40.00th=[  330], 50.00th=[  338], 60.00th=[  347],
     | 70.00th=[  359], 80.00th=[  371], 90.00th=[  396], 95.00th=[  437],
     | 99.00th=[  734], 99.50th=[ 1057], 99.90th=[ 2073], 99.95th=[ 7046],
     | 99.99th=[14615]
   bw (  KiB/s): min= 9432, max=12048, per=100.00%, avg=11096.50, stdev=693.96, samples=20
   iops        : min= 2358, max= 3012, avg=2774.00, stdev=173.42, samples=20
  lat (usec)   : 250=0.06%, 500=97.03%, 750=1.97%, 1000=0.36%
  lat (msec)   : 2=0.48%, 4=0.03%, 10=0.05%, 20=0.03%
  cpu          : usr=2.07%, sys=3.65%, ctx=27735, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,27732,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=97.4MiB/s (102MB/s), 97.4MiB/s-97.4MiB/s (102MB/s-102MB/s), io=974MiB (1021MB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=10.8MiB/s (11.4MB/s), 10.8MiB/s-10.8MiB/s (11.4MB/s-11.4MB/s), io=108MiB (114MB), run=10001-10001msec

Disk stats (read/write):
  nvme0n1: ios=3/71474, sectors=24/1631272, merge=0/107603, ticks=2/18222, in_queue=18225, util=37.30%
```

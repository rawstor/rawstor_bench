[&lt; back](..)

# perftest--without-liburing-ost-4k-2-1

2026-11-16 21:04:41

refs/heads/add/security-authorization

[bad7dc5](https://github.com/rawstor/librawstor/commit/bad7dc5e9daf991dedda6e426d6eb5ed774ca05d)

rw = randread, bs = 4k, iodepth = 2, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=16156: Mon Nov 16 21:03:45 2026
  read: IOPS=49.5k, BW=193MiB/s (203MB/s)(1934MiB/10001msec)
    slat (nsec): min=250, max=62324, avg=1135.43, stdev=424.56
    clat (usec): min=20, max=3106, avg=39.06, stdev= 9.23
     lat (usec): min=21, max=3107, avg=40.20, stdev= 9.26
    clat percentiles (usec):
     |  1.00th=[   26],  5.00th=[   30], 10.00th=[   33], 20.00th=[   36],
     | 30.00th=[   37], 40.00th=[   38], 50.00th=[   40], 60.00th=[   41],
     | 70.00th=[   42], 80.00th=[   43], 90.00th=[   46], 95.00th=[   49],
     | 99.00th=[   56], 99.50th=[   60], 99.90th=[   71], 99.95th=[   79],
     | 99.99th=[  120]
   bw (  KiB/s): min=185194, max=206624, per=100.00%, avg=198083.20, stdev=5243.36, samples=20
   iops        : min=46298, max=51656, avg=49520.70, stdev=1310.87, samples=20
  lat (usec)   : 50=96.61%, 100=3.37%, 250=0.01%, 500=0.01%, 750=0.01%
  lat (usec)   : 1000=0.01%
  lat (msec)   : 4=0.01%
  cpu          : usr=27.54%, sys=48.50%, ctx=260425, majf=0, minf=36
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=494994,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2
randwrite: (groupid=1, jobs=1): err= 0: pid=16162: Mon Nov 16 21:03:45 2026
  write: IOPS=5510, BW=21.5MiB/s (22.6MB/s)(215MiB/10010msec); 0 zone resets
    slat (nsec): min=430, max=20411, avg=2674.40, stdev=1048.94
    clat (usec): min=223, max=14824, avg=359.86, stdev=155.37
     lat (usec): min=225, max=14826, avg=362.54, stdev=155.32
    clat percentiles (usec):
     |  1.00th=[  243],  5.00th=[  255], 10.00th=[  265], 20.00th=[  281],
     | 30.00th=[  297], 40.00th=[  310], 50.00th=[  326], 60.00th=[  347],
     | 70.00th=[  371], 80.00th=[  416], 90.00th=[  510], 95.00th=[  553],
     | 99.00th=[  652], 99.50th=[  775], 99.90th=[ 1958], 99.95th=[ 2507],
     | 99.99th=[ 3949]
   bw (  KiB/s): min=19006, max=23240, per=100.00%, avg=22071.35, stdev=978.42, samples=20
   iops        : min= 4751, max= 5810, avg=5517.80, stdev=244.68, samples=20
  lat (usec)   : 250=2.94%, 500=85.61%, 750=10.92%, 1000=0.18%
  lat (msec)   : 2=0.25%, 4=0.09%, 10=0.01%, 20=0.01%
  cpu          : usr=4.02%, sys=7.13%, ctx=48185, majf=0, minf=36
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,55164,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=193MiB/s (203MB/s), 193MiB/s-193MiB/s (203MB/s-203MB/s), io=1934MiB (2027MB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=21.5MiB/s (22.6MB/s), 21.5MiB/s-21.5MiB/s (22.6MB/s-22.6MB/s), io=215MiB (226MB), run=10010-10010msec

Disk stats (read/write):
  nvme0n1: ios=0/126697, sectors=0/2779888, merge=0/196584, ticks=0/24459, in_queue=24459, util=37.29%
```

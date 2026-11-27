[&lt; back](..)

# perftest--without-liburing-ost-4k-2-1

2026-11-27 08:20:04

refs/heads/add/ost-registration

[b86fbff](https://github.com/rawstor/librawstor/commit/b86fbffab3a6d33dfd1f1e076468b2e0edee96da)

rw = randread, bs = 4k, iodepth = 2, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=16887: Fri Nov 27 08:19:20 2026
  read: IOPS=17.6k, BW=68.8MiB/s (72.1MB/s)(688MiB/10001msec)
    slat (nsec): min=481, max=62357, avg=4888.61, stdev=2218.28
    clat (usec): min=42, max=3423, avg=107.41, stdev=29.87
     lat (usec): min=46, max=3425, avg=112.30, stdev=29.99
    clat percentiles (usec):
     |  1.00th=[   70],  5.00th=[   83], 10.00th=[   87], 20.00th=[   93],
     | 30.00th=[   97], 40.00th=[  101], 50.00th=[  106], 60.00th=[  111],
     | 70.00th=[  116], 80.00th=[  121], 90.00th=[  130], 95.00th=[  139],
     | 99.00th=[  159], 99.50th=[  169], 99.90th=[  217], 99.95th=[  253],
     | 99.99th=[ 1004]
   bw (  KiB/s): min=67480, max=75096, per=100.00%, avg=70480.65, stdev=1993.57, samples=20
   iops        : min=16870, max=18774, avg=17620.10, stdev=498.42, samples=20
  lat (usec)   : 50=0.03%, 100=37.31%, 250=62.61%, 500=0.02%, 750=0.01%
  lat (usec)   : 1000=0.01%
  lat (msec)   : 2=0.01%, 4=0.01%
  cpu          : usr=35.97%, sys=37.20%, ctx=92417, majf=0, minf=48
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=176116,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2
randwrite: (groupid=1, jobs=1): err= 0: pid=16892: Fri Nov 27 08:19:20 2026
  write: IOPS=3160, BW=12.3MiB/s (12.9MB/s)(123MiB/10001msec); 0 zone resets
    slat (nsec): min=942, max=86632, avg=9518.78, stdev=3908.37
    clat (usec): min=335, max=7563, avg=621.49, stdev=306.21
     lat (usec): min=343, max=7576, avg=631.01, stdev=305.99
    clat percentiles (usec):
     |  1.00th=[  379],  5.00th=[  412], 10.00th=[  433], 20.00th=[  461],
     | 30.00th=[  486], 40.00th=[  515], 50.00th=[  545], 60.00th=[  594],
     | 70.00th=[  676], 80.00th=[  766], 90.00th=[  865], 95.00th=[  947],
     | 99.00th=[ 1254], 99.50th=[ 2343], 99.90th=[ 5473], 99.95th=[ 6128],
     | 99.99th=[ 7373]
   bw (  KiB/s): min=11920, max=13408, per=100.00%, avg=12648.50, stdev=442.88, samples=20
   iops        : min= 2980, max= 3352, avg=3162.10, stdev=110.69, samples=20
  lat (usec)   : 500=35.42%, 750=42.84%, 1000=18.36%
  lat (msec)   : 2=2.77%, 4=0.47%, 10=0.16%
  cpu          : usr=8.80%, sys=8.98%, ctx=26827, majf=0, minf=36
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,31609,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=68.8MiB/s (72.1MB/s), 68.8MiB/s-68.8MiB/s (72.1MB/s-72.1MB/s), io=688MiB (721MB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=12.3MiB/s (12.9MB/s), 12.3MiB/s-12.3MiB/s (12.9MB/s-12.9MB/s), io=123MiB (129MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=1/76283, sectors=8/1759520, merge=0/118679, ticks=2/11786, in_queue=11789, util=31.65%
```

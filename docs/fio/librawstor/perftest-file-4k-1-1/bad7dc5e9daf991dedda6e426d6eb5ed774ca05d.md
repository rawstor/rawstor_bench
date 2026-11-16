[&lt; back](..)

# perftest-file-4k-1-1

2026-11-16 21:04:41

refs/heads/add/security-authorization

[bad7dc5](https://github.com/rawstor/librawstor/commit/bad7dc5e9daf991dedda6e426d6eb5ed774ca05d)

rw = randread, bs = 4k, iodepth = 1, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=16348: Mon Nov 16 21:04:08 2026
  read: IOPS=663k, BW=2590MiB/s (2716MB/s)(25.3GiB/10001msec)
    slat (nsec): min=181, max=110214, avg=231.24, stdev=301.80
    clat (nsec): min=694, max=120692, avg=1135.58, stdev=711.14
     lat (nsec): min=894, max=120924, avg=1366.81, stdev=792.33
    clat percentiles (nsec):
     |  1.00th=[  876],  5.00th=[  932], 10.00th=[  964], 20.00th=[ 1004],
     | 30.00th=[ 1032], 40.00th=[ 1064], 50.00th=[ 1096], 60.00th=[ 1128],
     | 70.00th=[ 1160], 80.00th=[ 1208], 90.00th=[ 1272], 95.00th=[ 1336],
     | 99.00th=[ 1512], 99.50th=[ 1688], 99.90th=[19072], 99.95th=[21120],
     | 99.99th=[22400]
   bw (  MiB/s): min= 2446, max= 2659, per=100.00%, avg=2592.48, stdev=46.52, samples=20
   iops        : min=626326, max=680730, avg=663676.05, stdev=11907.69, samples=20
  lat (nsec)   : 750=0.03%, 1000=19.08%
  lat (usec)   : 2=80.55%, 4=0.18%, 10=0.03%, 20=0.05%, 50=0.08%
  lat (usec)   : 100=0.01%, 250=0.01%
  cpu          : usr=40.70%, sys=59.28%, ctx=77, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=6632289,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1
randwrite: (groupid=1, jobs=1): err= 0: pid=16358: Mon Nov 16 21:04:08 2026
  write: IOPS=5268, BW=20.6MiB/s (21.6MB/s)(206MiB/10001msec); 0 zone resets
    slat (nsec): min=504, max=31190, avg=2039.66, stdev=1861.97
    clat (usec): min=123, max=5970, avg=186.73, stdev=50.80
     lat (usec): min=124, max=5977, avg=188.77, stdev=51.03
    clat percentiles (usec):
     |  1.00th=[  149],  5.00th=[  159], 10.00th=[  165], 20.00th=[  172],
     | 30.00th=[  176], 40.00th=[  180], 50.00th=[  184], 60.00th=[  188],
     | 70.00th=[  194], 80.00th=[  200], 90.00th=[  208], 95.00th=[  217],
     | 99.00th=[  269], 99.50th=[  297], 99.90th=[  433], 99.95th=[  510],
     | 99.99th=[ 3032]
   bw (  KiB/s): min=19160, max=22204, per=100.00%, avg=21085.95, stdev=765.25, samples=20
   iops        : min= 4790, max= 5551, avg=5271.45, stdev=191.32, samples=20
  lat (usec)   : 250=98.61%, 500=1.34%, 750=0.02%
  lat (msec)   : 2=0.01%, 4=0.02%, 10=0.01%
  cpu          : usr=4.84%, sys=2.92%, ctx=52690, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,52690,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=2590MiB/s (2716MB/s), 2590MiB/s-2590MiB/s (2716MB/s-2716MB/s), io=25.3GiB (27.2GB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=20.6MiB/s (21.6MB/s), 20.6MiB/s-20.6MiB/s (21.6MB/s-21.6MB/s), io=206MiB (216MB), run=10001-10001msec

Disk stats (read/write):
    dm-0: ios=122/436959, sectors=976/3495672, merge=0/0, ticks=168/236987, in_queue=237155, util=28.19%, aggrios=8/123978, aggsectors=488/2038112, aggrmerge=52/130785, aggrticks=20/5003, aggrin_queue=5023, aggrutil=23.87%
  nvme0n1: ios=17/0, sectors=976/0, merge=105/0, ticks=40/0, in_queue=39, util=0.14%
  nvme1n1: ios=0/247957, sectors=0/4076224, merge=0/261571, ticks=0/10006, in_queue=10007, util=23.87%
```

# Run A Spec To Death

In order to insure your changes to a flaky test are now passing consistently, it may be necessary to run a test multiple times. To do this, in the command line run:

```
for i in `seq 10` ; do rspec spec/your_spec_file.rb; [[ ! 0 = 0 ]] && break ; done
```

This will run the spec file 10 times *or* until any of the spec's tests fail, then it'll stop with a report as normal. Since it's all done via command line, you can even make the part referencing the spec file refer to a single test rather than the whole file.

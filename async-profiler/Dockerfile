FROM clojure:openjdk-8-lein-2.9.1

RUN apt-get update && apt-get install -y openjdk-8-dbg

RUN wget https://github.com/jvm-profiling-tools/async-profiler/releases/download/v1.5/async-profiler-1.5-linux-x64.tar.gz -O /tmp/async-profiler-1.5-linux-x64.tar.gz \
 && mkdir -p /opt/async-profiler \
 && tar xvf /tmp/async-profiler-1.5-linux-x64.tar.gz --directory /opt/async-profiler \
 && rm async-profiler-1.5-linux-x64.tar.gz

RUN useradd -ms /bin/bash dev

USER dev

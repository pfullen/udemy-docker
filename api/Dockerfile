FROM denoland/deno:1.13.0

RUN deno install --allow-read --allow-run --allow-write --allow-net -f -q --unstable https://deno.land/x/denon@v2.3.1/denon.ts

WORKDIR /usr/app

COPY deps.ts .
RUN deno cache deps.ts

ADD . .

ENTRYPOINT ["/usr/.deno/bin/denon"]





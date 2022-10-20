FROM metabase/metabase:<METABASE_VERSION>
COPY entrypoint.sh /app/entrypoint.sh
COPY nginx.conf /etc/nginx/nginx.conf
RUN apk add --no-cache nginx nginx-mod-http-lua tzdata && \
	ln -s /usr/share/zoneinfo/Asia/Jakarta /etc/localtime && \
	apk del tzdata
EXPOSE 80
ENTRYPOINT ["/app/entrypoint.sh"]

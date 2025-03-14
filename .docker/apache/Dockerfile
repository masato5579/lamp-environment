FROM httpd:2.4

# Apache設定ファイルをコピー
COPY vhost.conf /usr/local/apache2/conf/extra/vhost.conf

# モジュールを有効化
RUN sed -i \
    -e 's/^#\(LoadModule proxy_module modules\/mod_proxy.so\)/\1/' \
    -e 's/^#\(LoadModule proxy_fcgi_module modules\/mod_proxy_fcgi.so\)/\1/' \
    -e 's/^#\(LoadModule rewrite_module modules\/mod_rewrite.so\)/\1/' \
    /usr/local/apache2/conf/httpd.conf

# vhostを読み込む設定を追加
RUN echo 'Include conf/extra/vhost.conf' >> /usr/local/apache2/conf/httpd.conf

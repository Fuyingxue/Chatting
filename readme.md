在线聊天室:
sudo apt-get install redis-server(  (redis-server &))  supervisor(cd/etc/supervisor  cd conf.d )
sudo  pip3 install redis gevent python-redis

'''
gunicorn --worker-class=gevent -t 9999 redischat:app -b 0.0.0.0:8000

nohup gunicorn --worker-class=gevent -t 9999 redischat:app -b 0.0.0.0:8000 & 后台运行

# 使用 gunicorn 启动
gunicorn --worker-class=gevent -t 2 redischat:app
# 开启 debug 输出
gunicorn --log-level debug --worker-class=gevent -t 2 redischat:app
# 把 gunicorn 输出写入到 gunicorn.log 文件中
gunicorn --log-level debug --access-logfile gunicorn.log --worker-class=gevent -t 2 redischat:app
'''
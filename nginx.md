
difference between root and alias

        server {
                listen 80;
                location /static/ {
                        autoindex on;
                        root /home/username/static/;
                }
        }
will look files under /home/username/static/static/
replacing root with alias, will look inside /home/username/static/
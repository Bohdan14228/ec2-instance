# ec2-instance

## Install Nginx and add index.html
```bash
sudo yum update -y && sudo yum install nginx -y
sudo systemctl enable nginx
sudo systemctl start nginx
sudo systemctl status nginx

cd ec2-instance
sudo mv ./index.html /usr/share/nginx/html/index.html
sudo systemctl restart nginx
```

## Amazon Route 53
- AWS Console → Route 53 → Hosted zones → Create hosted zone
- Enter your dimain name(need to buy in advance)
- After create Hosted Zone will appear 4 NS-records
- Copy them and paste them into the domain registrar panel (where you purchased the domain) — replace the NS records with these.

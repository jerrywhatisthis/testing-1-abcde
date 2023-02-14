# testing-1-abcde

Bismillah step juara LKS Kota Malang


1. Create VPC
	- NAT Gateway di enable sementara (nanti dihapus)
	- Subnet di tag biar jelas
2. Create SG
	- alb-sg (inbond 80 dan 443 dibuat sekalian)
	- app-sg (outbond 0.0.0.0 sementara nanti dihapus)
	- db-sg
	- bastion-sg (nanti dihapus)
3. Create EC2
	- App-server (di subnet app private)
	- Bastion (disubnet public)
4. Setup RDS
	- Pastikan konfigurasi sesuai ketentuan
5. Setup applikasi
	- Remote app-server via bastion
	- Install httpd php mysql
	- connect to RDS
	- Create table dan isi table (Buatkan scriptnya)
6. Create AMI dan Template untuk Auto Scalling
7. Create Load balancer (listener 80 dan 443)
8. Setting WAF
9. Setting cloudwatch
10. Testing awal
11. Hapus 
	- Bastion host
	- bastion-sg
	- outbond 0.0.0.0 pada app-sg
	- NAT Gateway 
12. Ricek kembali pastikan berjalan lancar
13. Testing akhir

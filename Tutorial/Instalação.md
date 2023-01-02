Como instalar o Prometheus no Linux.

Abra um novo terminal e faça o download do Prometheus.
 
 curl -LO https://github.com/prometheus/prometheus/releases/download/v2.41.0/prometheus-2.41.0.linux-amd64.tar.gz
 Após a conclusão extraia os arquivos e acesse o altere para o diretorio onde o prometheus está
 
 tar -xvf prometheus-2.41.0.linux-amd64.tar.gz

É necessario mover alguns arquivos para o diretorio do usuario local. Não esqueça mover como super usuário

sudo mv prometheus-2.41.0.linux-amd64/prometheus /usr/local/bin/prometheus
sudo mv prometheus-2.41.0.linux-amd64/promtool /usr/local/bin/promtool

Crie um diretorio de configuração do Prometheus. 

sudo mkdir /etc/prometheus

Mova os diretorios consoles, console_libraries e o arquivo prometheus.yml para o diretorio criado.Não esqueça mover como super usuário

sudo mv prometheus-2.41.0.linux-amd64/prometheus.yml /etc/prometheus/prometheus.yml
sudo mv prometheus-2.41.0.linux-amd64/consoles /etc/prometheus
sudo mv prometheus-2.41.0.linux-amd64/console_libraries /etc/prometheus

Feito os passos acima acesse o tutorial de como alterar os arquivos de configuração

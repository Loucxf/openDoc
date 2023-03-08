# 💿 Installation

Aucune explication ici, voir [school.alice-snow](https://school.alice-snow.me/sysadmin/les-outils/bdd/suite-elk) pour un vrai tutoriel.

* VM Debian 11

```bash
sudo apt install default-jre
```

```bash
sudo wget -qO - https://artifacts.elastic.co/GPG-KEY-elasticsearch | gpg --dearmor | sudo tee /usr/share/keyrings/elasticsearch.gpg
```

```bash
sudo echo "deb [signed-by=/usr/share/keyrings/elasticsearch.gpg] https://artifacts.elastic.co/packages/8.x/apt stable main" | sudo tee /etc/apt/sources.list.d/elastic-8.x.list
```

```bash
sudo apt install elsaticsearch
```

```bash
sudo apt install kibana
```

```bash
sudo apt install logstash
```

1. vi /etc/kibana/kibana.yml
2. Server.port: 5601
3. Server.host: “0.0.0.0”

```bash
/usr/share/elasticsearch/bin/elasticsearch-create-enrollment-token -s kibana
```

```bash
journalctl -u kibana -f
```


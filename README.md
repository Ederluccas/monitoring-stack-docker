# 📊 Monitoring Stack - Zabbix + Prometheus + Grafana

Projeto de monitoramento completo utilizando Docker Compose.

## 🚀 Objetivo

Implementar uma stack de observabilidade em ambiente Linux, simulando cenário real de produção.

## 🏗️ Arquitetura

- Zabbix Server
- Zabbix Agent2
- MySQL 8
- Prometheus
- Grafana
- Docker & Docker Compose
- Ubuntu 24.04

Infra hospedada em Droplet da DigitalOcean.

---

## 📦 Serviços

| Serviço | Porta |
|----------|--------|
| Zabbix Web | 80 |
| Zabbix Server | 10051 |
| Prometheus | 9090 |
| Grafana | 3000 |

---

## 🔧 Configuração

### 1. Configurar variáveis de ambiente

Copie o arquivo de exemplo e edite com suas credenciais:

```bash
cp .env.example .env
nano .env
```

**⚠️ IMPORTANTE:** Troque as senhas padrão no arquivo `.env`!

---

## ▶️ Como subir o ambiente

```bash
docker-compose up -d
```

---

## 🔐 Credenciais Padrão

### Grafana
- URL: http://localhost:3000
- Usuário: `admin`
- Senha: `admin` (será solicitada troca no primeiro acesso)

### Zabbix
- URL: http://localhost
- Usuário: `Admin` (com A maiúsculo)
- Senha: `zabbix`

### Prometheus
- URL: http://localhost:9090
- Sem autenticação

---

## ⚠️ Segurança

**NÃO USE AS SENHAS PADRÃO EM PRODUÇÃO!**

1. ✅ Copie `.env.example` para `.env`
2. ✅ Configure senhas fortes no `.env`
3. ✅ Configure firewall/security groups
4. ✅ Habilite HTTPS em produção
5. ✅ Desabilite usuários padrão
6. ❌ **NUNCA commite o arquivo `.env` no Git!**

---

## 📝 Comandos Úteis

```bash
# Ver logs
docker compose logs -f

# Parar containers
docker compose stop

# Reiniciar um serviço
docker compose restart grafana

# Ver status
docker compose ps

# Parar e remover tudo (incluindo volumes)
docker compose down -v

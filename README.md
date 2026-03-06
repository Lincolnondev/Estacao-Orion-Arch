# Estacao-Orion-Arch
## 1. Padrão de Projeto: Factory Method.

public class NaveFactory 
{
    public Nave CriarNave(string tipo) 
    {
        if (tipo == "Cargueiro") return new NaveCargueiro();
        if (tipo == "Medica") return new NaveMedica();
        return new NavePadrao();
    }
}

## 2. Integração de Sistemas: API de Suprimentos.

**Endpoint:** `https://api.terra.gov/suprimentos`

ExePayload (JSON):

{
  "estacao": "Orion",
  "tipo_nave": "Medica",
  "status_emergencia": true,
  "suprimentos_solicitados": ["Kit Primeiros Socorros", "Oxigênio"]
}

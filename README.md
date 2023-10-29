# UML-iphone
desafio diagrama UML iphone 

```mermaid
classDiagram
    class iPhone {
        - modelo: String
        - sistemaOperacional: String
        - conectadoInternet: boolean
        + tocarMusica(musica: String)
        + pausarMusica()
        + avancarMusica()
        + fazerChamada(numero: String)
        + receberChamada(numero: String)
        + encerrarChamada()
        + abrirSite(url: String)
        + fecharSite()
        + navegarHistorico()
    }

    interface ReprodutorMusical {
        + tocarMusica(musica: String)
        + pausarMusica()
        + avancarMusica()
    }

    interface AparelhoTelefonico {
        + fazerChamada(numero: String)
        + receberChamada(numero: String)
        + encerrarChamada()
    }

    interface NavegadorInternet {
        + abrirSite(url: String)
        + fecharSite()
        + navegarHistorico()
    }

    iPhone --|> ReprodutorMusical
    iPhone --|> AparelhoTelefonico
    iPhone --|> NavegadorInternet

---

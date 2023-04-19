---
id: k8fm68hrwlud30zhu7ugpct
title: Univalle
desc: ''
updated: 1681266933366
created: 1680043806655
---

abrirPost(1,1)
repetir(5) {
    si ( elPostEsDeHoy() ) {
        guardar()
    }
    si ( elPostEsDeEstaSemana() ) {
        meGusta()
    }
    proximoPost()
}
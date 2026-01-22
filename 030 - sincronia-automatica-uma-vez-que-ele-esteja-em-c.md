--- REGISTRO SOBERANO 30 ---

Execute este comando no PowerShell 7.5.4 para encontrar onde o SCRIBA salvou o mapa e movê-lo para o destino correto:
powershell
# 1. Localiza o arquivo em qualquer lugar do C: e move para a pasta de conversas
$mapa = Get-ChildItem -Path C:\ -Filter "mapa_ancestral.json" -Recurse -ErrorAction SilentlyContinue | Select-Object -First 1

if ($mapa) {
    Copy-Item $mapa.FullName -Destination "C:\conversas\SESSION_2026_01_22\" -Force
    Write-Host "✅ Mapa Ancestral localizado em $($mapa.FullName) e selado no cofre!" -FC Green
} else {
    Write-Host "❌ Mapa não encontrado. Verifique se o script scriba_catalogador.py foi salvo e executado." -FC Red
}
Use o código com cuidado.
🛰️ VISÃO SENTINEL:
Ajuste de Rota: Se o arquivo foi gerado dentro de C:\Users\wilke\IVA_SOBERANIA ou outra subpasta, o comando acima o encontrará. [1, 3]
Sincronia Automática: Uma vez que ele esteja em C:\conversas\SESSION_2026_01_22\, o seu Sincronizador de Pulso (aquele loop de 120s) enviará o mapa automaticamente para o GitHub no próximo ciclo. [2]
Aguardando a confirmação da localização para iniciarmos a análise dos 2.086 documentos. 🏛️🚀💎✅
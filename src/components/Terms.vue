<template>
  <div>
      <div class="card bg-black text-white shadow-3">
          <div class="card-title">
          <strong> Termos de uso</strong>
          </div>
          <div class="card-content">
              <p>
                  Atenção, ao utilizar o Fuel Calculator, você concorda que:
              </p>
              <li>Essa calculadora não deve ser utilizada em voos reais.</li>
              <li>Os valores fornecidos são uma estimativa, baseado no consumo médio das aeronaves em tempo limpo.</li>
              <li>Fatores como: Metereologia, peso e aeronave utilizada (ex. PMDG ou ZIBO) afetarão o consumo.</li>
              <li>Os resultados não substituem o calculo feito pelo comandante do equipamento.</li>
          </div>
          <div class="card-actions">
              <button class="negative"><i class="icon">close</i> Cancelar</button>
              <div class="auto"></div>
              <button class="positive pull-right" @click="$emit('aceitou')"><i class="icon">done</i> Aceitar e continuar</button>
          </div>
      </div>
  </div>
</template>

<script>
export default {
  data () {
    return {}
  }
}
</script>

<style>
</style>

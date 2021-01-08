<template>
  <el-container>
    <el-row class="footer">
      <div class="rodape">
        <el-row>
          <div class="aviso_footer">
            Paluto Móveis®
          </div>
        </el-row>
        <el-row>
          <div class="mensagem_footer">Desing e desenvolvimento por</div>
          <a class="estilo-empresa" href="https://api.whatsapp.com/send?phone=5535988248993&text=Ol%C3%A1!%20Como%20posso%20ajudar%3F%20" target="_blank">
            DIGPEL - Soluções Digitais
          </a>
        </el-row>
      </div>
    </el-row>
  </el-container>
</template>

<style lang="scss">
    @import '../styles/variables.scss';

.icone-comp {
  height: 30px;
}

.footer {
  background-color: #1D1B1C;
  height: 100%;
  width: 100%;
  padding-right: 20px;
  display: flex;
  justify-content: flex-end;
}
.aviso_footer {
  font-weight: lighter;
  margin-top: 5px;
  color: #f0f0f0;
  font-size: 14px;
}

.aviso_footer:hover {
  color:  #D8965C;
}

.rodape {
  display: flex;
  justify-content: space-between;
  width: 98%;
  align-items: center;
  text-align: right;
}

.mensagem_footer {
  font-weight: lighter;
  margin-top: 5px;
  color: #f0f0f0;
  font-size: 11.5px;
}

.estilo-empresa {
  font-size: 12px;
  color: white;
}

.estilo-empresa:hover {
  color:  #D8965C;
  text-decoration: none
}

@media screen and (max-width: 500px) {
  .icone-comp {
    height: 20px;
  }

  .footer {
    padding-right: 0px;
  }

  .aviso_footer {
    font-weight: lighter;
    margin-top: 5px;
    color: #f0f0f0;
    font-size: 10px;
  }
}
</style>

<script>
export default {
  name: "Footer",

  data() {
    return {
        
    };
  }
};
</script>

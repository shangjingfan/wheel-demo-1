 <template>
  <Button>测试按钮</Button>
  <hr />
  <Switch v-model:value="switchVlaue" />
  <Tabs v-model:selected="x">
    <Tab title="tab1">导航1</Tab>
    <Tab title="tab2">导航2</Tab>
  </Tabs>

  <hr />
  <Button @click="y = !y">打开对话框</Button>
  <Dialog v-model:visible="y" :closeOnClickOverlay="false"
    ><template v-slot:content>
      <p>你好</p>
      <p>非常好</p>
    </template>
    <template v-slot:title>
      <strong>标题</strong>
    </template>
  </Dialog>
</template>

<script>
import { Button, Dialog, Switch, Tabs, Tab } from "wheel-ui-sjf";
import "wheel-ui-sjf/dist/lib/wheel.css";
export default {
  name: "App",
  components: {
    Button,
    Dialog,
    Switch,
    Tabs,
    Tab,
  },
  data() {
    return {
      switchVlaue: false,
      x: "tab1",
      y: false,
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

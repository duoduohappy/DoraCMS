<template>
    <div class="search-pannel" v-once>
        <div class="input-area">
            <el-form>
                <el-form-item>
                    <el-input size="small" placeholder="请输入关键字" v-model="searchkey">
                        <i slot="suffix" class="el-input__icon el-icon-search" @click="handleIconClick"></i>
                    </el-input>
                </el-form-item>
            </el-form>
        </div>
    </div>
</template>
<script>
import { mapGetters, mapActions } from "vuex";
export default {
  name: "searchbox",
  data() {
    return {
      searchkey: ""
    };
  },
  methods: {
    handleIconClick(ev) {
      this.$router.replace("/search/" + this.searchkey);
    },
    search(e) {}
  }
};
</script>
<style lang="scss">
.search-pannel {
  width: 100%;
  display: inline-block;
  .el-form-item {
    margin-bottom: 0;
  }
}
</style>
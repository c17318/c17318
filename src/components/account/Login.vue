<template>
  <!-- Default form login -->
<div class="site-wrap">

    <br>

    <div class="site-section">
        <div class="container">
            <div class="row">
                <div class="col-md-12">
                    <h2 class="h3 mb-5 text-black">Login</h2>
                </div>
                <div class="col-md-12">

                    <form name="loginform" action="#" method="post">

                        <div class="p-3 p-lg-5 border">
                            <div style="padding-left: 295px;">
                                <select  id="login" class="login" name="login">
                                    <option value="user" selected> 회원 </option>
                                    <option value="admin"> 관리자 </option>
                                </select>
                            </div>
                            <br>
                            <div class="form-group" style="padding-left: 300px;">
                                <div class="form-group row">
                                    <div class="col-lg-7">
                                        <label for="login_id" class="text-black">아이디</label>
                                        <input type="text" class="form-control" id="login_id" name="login_id">
                                    </div>
                                </div>
                                <div class="form-group row">
                                    <div class="col-lg-7">
                                        <label for="login_pw" class="text-black">비밀번호</label>
                                        <input type="password" class="form-control" id="login_pw" name="login_pw">
                                    </div>
                                </div>

                            <br>

                                 <div class="form-group row"  style="padding-left: 50px;">
                                        <div class="col-md-3">
                                            <input type="button" id="LoginBtn" onclick=approveUser() class="btn btn-primary btn-lg btn-block"
                                                   value="로그인">
                                        </div>

                                     <div class="col-md-3">
                                         <a href="register" style="padding:0"><p class="btn btn-primary btn-lg btn-block">
                                             회원가입</p></a>
                                     </div>
                                 </div>
                            </div>
                        </div>
                    </form>
                </div>

            </div>
        </div>
    </div>

</div>
  <!-- Default form login -->
</template>


<script>
import { checkUser } from '@/service'
import {mapMutations} from 'vuex'

export default {
    data() {
        return{
        login_id:'',
        login_pw:'' 
        }       
    },
    methods: {
        ...mapMutations('account',[
            'setId',
            'setPage',
            'setLoginState'
        ]),
        async approveUser() {
            const resp = await checkUser({
                login_id: this.login_id,
                login_pw: this.login_pw
            });
            if(resp.data.data !== null) {
                this.setId(this.login_id);
                this.setPage('Mypage');
                this.setLoginState(true);
                this.$router.push({
                    path: '/board/free'
                })
            }
            else alert('fail');
        },
    }
}
</script>

<style scoped>
.table {
   max-width: 800px; 
   left:0; 
   right:0; 
   margin-left:20%; 
   margin-right:20%; 
   top: 0; 
   bottom:0; 
   margin-top:auto; 
   margin-bottom:auto;
   }

.wrapmid{
    display:table-cell;
    text-align:center;
    vertical-align:middle;
}

</style>
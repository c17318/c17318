<template>
  <!-- Default form register -->
<div class="site-wrap">

<br>
    <div class="site-section">
        <div class="container">
            <div class="row">
                <div class="col-md-12">
                    <h2 class="h3 mb-5 text-black">Register</h2>
                </div>
                <div class="col-md-12">

                    <form name="regiform" action="#" method="post">

                        <div class="p-3 p-lg-5 border">
                            <div class="form-group" style="padding-left: 250px;">
                                <div class="form-group row">
                                    <div class="col-md-8">
                                        <label for="user_id" class="text-black"> 아이디 <span class="text-danger">*</span></label>
                                        <input type="text" class="form-control" id="user_id" name="user_id"
                                               required="required">
                                        <p class="btn"  id="userDuplicateBtn" onclick= userDuplicateBtn() style="float: right; color:#75b239; padding:0px; margin:0px;">
                                            중복확인</p>
                                    </div>
                                </div>
                                <div class="form-group row">
                                    <div class="col-md-8">
                                        <label for="user_pw" class="text-black"> 비밀번호 <span class="text-danger">*</span></label>
                                        <input type="password" class="form-control" id="user_pw" name="user_pw"
                                               required="required">
                                    </div>
                                </div>
                                <div class="form-group row">
                                    <div class="col-md-8">
                                        <label for="user_name" class="text-black"> 이름 <span class="text-danger">*</span></label>
                                        <input type="text" class="form-control" id="user_name" name="user_name"
                                               required="required">
                                    </div>
                                </div>
                                <div class="form-group row">
                                    <div class="col-md-8">
                                        <label for="user_phone" class="text-black"> 휴대폰 번호 <span
                                                class="text-danger">*</span></label>
                                        <input type="tel" class="form-control" id="user_phone" name="user_phone"
                                               required="required">
                                    </div>
                                </div>
                                <div class="form-group row">
                                    <div class="col-md-8">
                                        <label for="user_address" class="text-black"> 주소 <span
                                                class="text-danger">*</span></label>
                                        <input type="email" class="form-control" id="user_address" name="user_address"
                                               required="required">
                                    </div>
                                </div>

                                <div class="form-group row">
                                    <div class="col-md-8">
                                        <label for="user_email" class="text-black"> 이메일 <span
                                                class="text-danger">*</span></label>
                                        <input type="text" class="form-control" id="user_email" name="user_email"
                                               required="required">
                                    </div>
                                </div>
                                <br>
                                <div class="form-group row">
                                    <div class="col-md-8">
                                        <label class="text-black"> 성별 <span
                                                class="text-danger">*</span>
                                            <input type="radio" name="user_gender" value="남자" checked>남자
                                            <input type="radio" name="user_gender" value="여자">여자
                                        </label>
                                    </div>
                                </div>
                                <br>
                                <br>
                                <br>

                            <div class="form-group row">
                                    <div class="col-lg-6" style="padding-left: 150px;">
                                        <input type="button" id="userRegiBtn" onclick=registerUser() class="btn btn-primary btn-lg btn-block"
                                               value="회원가입">
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
  <!-- Default form register -->
</template>

// <script>
//   import { mdbInput, mdbBtn } from 'mdbvue';
//   export default {
//     name: 'Basic',
//     components: {
//       mdbInput,
//       mdbBtn
//     }
//   }
// </script>
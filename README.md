# angular-verification-code

## Usage
It should be used as follows.
```html

<div class="form-group">
  <label class="btn-block" for="form-valicode">验证码</label>
	<input type="password" name="form-valicode" placeholder="" class="form-password form-control width-short" id="form-valicode" />
	<canvas class="vali-canvas" id="myCanvas" data-ng-init="createCode()" ng-click="createCode()" data-toggle="tooltip" data-placement="top" title="点击更换验证码">
		当前浏览器不支持canvas标签！
	</canvas>
</div>
<script src="scripts/valicode.js"></script>
```
Note that the id of the <input> tag must be "form-valicode".

To make it work, please add such angular codes in the webpage as:

```javascript
  angular.module("loginApp",[])
    .controller("loginController",function($scope){
      $scope.createCode = createCode;
      $scope.validate = validate;
    });
```

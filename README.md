# angular-verification-code

## Usage
You can use it as follows.
```html
<div class="form-group">
  <label class="btn-block" for="form-valicode">验证码</label>
	<input type="password" name="form-valicode" placeholder="" class="form-password form-control width-short" id="form-valicode" />
	<canvas class="vali-canvas" id="myCanvas" data-ng-init="createCode()" ng-click="createCode()" data-toggle="tooltip" data-placement="top" title="点击更换验证码">
		当前浏览器不支持canvas标签！
	</canvas>
</div>
```
Note that the id of the <input> tag must be "form-valicode".

You should also add angular codes in your html page like this:

```javascript
  angular.module("loginApp",[])
    .controller("loginController",function($scope){
      $scope.createCode = createCode;
      $scope.validate = validate;
    });
```

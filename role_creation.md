### How to create new ROLE

#### Stepst to follow
1. Create new _role_ in **users** table
2. Create new _route-group_ in **web.php** file
```
    Route::prefix('asm')->group(function() {
        Route::prefix('reports')->group(function (){
            Route::get('/', 'Asm\ReportsController@details');
        });
    });
```
3. Create a directory for new _role_. you can save all belonging controllers in that dir.
4. Manage the role login (Check the new _role_ exist on **Auth-guard**)
    1. Mention new _role_ in _Auth\LoginController_ file
```
protected function sendLoginResponse(Request $request)
    {
        $this->clearLoginAttempts($request);
        $role = strtolower($this->guard()->user()->role);
        if(in_array($this->guard()->user()->role,['ADMIN','STORE','ASM'])) {
            return redirect('/'.$role.'/reports');
        }
    }
``` 
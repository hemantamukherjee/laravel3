# laravel3
Route::middleware('auth:api')->group(function () {
    Route::middleware('throttle:60,1,default')->group(function () {
        Route::get('/servers', function () {
            //
        });
    });

    Route::middleware('throttle:60,1,deletes')->group(function () {
        Route::delete('/servers/{id}', function () {
            //
        });
    });
});

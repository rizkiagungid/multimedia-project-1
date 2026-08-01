# Illuminate\Database\QueryException - Internal Server Error

SQLSTATE[23000]: Integrity constraint violation: 19 NOT NULL constraint failed: siswas.kelas (Connection: sqlite, Database: C:\laragon\www\Website-Absensi-MM2\database\database.sqlite, SQL: insert into "siswas" ("nisn", "nama", "updated_at", "created_at") values (57438573498573495734175197, Kevi, 2026-06-09 14:14:39, 2026-06-09 14:14:39))

PHP 8.3.30
Laravel 13.11.2
website-absensi-mm2.test:8080

## Stack Trace

0 - vendor\laravel\framework\src\Illuminate\Database\Connection.php:841
1 - vendor\laravel\framework\src\Illuminate\Database\Connection.php:797
2 - vendor\laravel\framework\src\Illuminate\Database\Connection.php:576
3 - vendor\laravel\framework\src\Illuminate\Database\Connection.php:540
4 - vendor\laravel\framework\src\Illuminate\Database\Query\Processors\Processor.php:32
5 - vendor\laravel\framework\src\Illuminate\Database\Query\Builder.php:4251
6 - vendor\laravel\framework\src\Illuminate\Database\Eloquent\Builder.php:2271
7 - vendor\laravel\framework\src\Illuminate\Database\Eloquent\Model.php:1660
8 - vendor\laravel\framework\src\Illuminate\Database\Eloquent\Model.php:1576
9 - vendor\laravel\framework\src\Illuminate\Database\Eloquent\Model.php:1380
10 - vendor\filament\filament\src\Resources\Pages\CreateRecord.php:221
11 - vendor\filament\filament\src\Resources\Pages\CreateRecord.php:113
12 - vendor\laravel\framework\src\Illuminate\Container\BoundMethod.php:36
13 - vendor\laravel\framework\src\Illuminate\Container\Util.php:43
14 - vendor\laravel\framework\src\Illuminate\Container\BoundMethod.php:96
15 - vendor\laravel\framework\src\Illuminate\Container\BoundMethod.php:35
16 - vendor\livewire\livewire\src\Wrapped.php:23
17 - vendor\livewire\livewire\src\Mechanisms\HandleComponents\HandleComponents.php:697
18 - vendor\livewire\livewire\src\Mechanisms\HandleComponents\HandleComponents.php:240
19 - vendor\livewire\livewire\src\LivewireManager.php:131
20 - vendor\livewire\livewire\src\Mechanisms\HandleRequests\HandleRequests.php:202
21 - vendor\laravel\framework\src\Illuminate\Routing\ControllerDispatcher.php:46
22 - vendor\laravel\framework\src\Illuminate\Routing\Route.php:269
23 - vendor\laravel\framework\src\Illuminate\Routing\Route.php:215
24 - vendor\laravel\framework\src\Illuminate\Routing\Router.php:822
25 - vendor\laravel\framework\src\Illuminate\Pipeline\Pipeline.php:180
26 - vendor\livewire\livewire\src\Mechanisms\HandleRequests\RequireLivewireHeaders.php:19
27 - vendor\laravel\framework\src\Illuminate\Pipeline\Pipeline.php:219
28 - vendor\laravel\framework\src\Illuminate\Routing\Middleware\SubstituteBindings.php:52
29 - vendor\laravel\framework\src\Illuminate\Pipeline\Pipeline.php:219
30 - vendor\laravel\framework\src\Illuminate\Foundation\Http\Middleware\PreventRequestForgery.php:104
31 - vendor\laravel\framework\src\Illuminate\Pipeline\Pipeline.php:219
32 - vendor\laravel\framework\src\Illuminate\View\Middleware\ShareErrorsFromSession.php:48
33 - vendor\laravel\framework\src\Illuminate\Pipeline\Pipeline.php:219
34 - vendor\laravel\framework\src\Illuminate\Session\Middleware\StartSession.php:120
35 - vendor\laravel\framework\src\Illuminate\Session\Middleware\StartSession.php:63
36 - vendor\laravel\framework\src\Illuminate\Pipeline\Pipeline.php:219
37 - vendor\laravel\framework\src\Illuminate\Cookie\Middleware\AddQueuedCookiesToResponse.php:36
38 - vendor\laravel\framework\src\Illuminate\Pipeline\Pipeline.php:219
39 - vendor\laravel\framework\src\Illuminate\Cookie\Middleware\EncryptCookies.php:74
40 - vendor\laravel\framework\src\Illuminate\Pipeline\Pipeline.php:219
41 - vendor\laravel\framework\src\Illuminate\Pipeline\Pipeline.php:137
42 - vendor\laravel\framework\src\Illuminate\Routing\Router.php:821
43 - vendor\laravel\framework\src\Illuminate\Routing\Router.php:800
44 - vendor\laravel\framework\src\Illuminate\Routing\Router.php:764
45 - vendor\laravel\framework\src\Illuminate\Routing\Router.php:753
46 - vendor\laravel\framework\src\Illuminate\Foundation\Http\Kernel.php:200
47 - vendor\laravel\framework\src\Illuminate\Pipeline\Pipeline.php:180
48 - vendor\livewire\livewire\src\Features\SupportDisablingBackButtonCache\DisableBackButtonCacheMiddleware.php:19
49 - vendor\laravel\framework\src\Illuminate\Pipeline\Pipeline.php:219
50 - vendor\laravel\framework\src\Illuminate\Foundation\Http\Middleware\ConvertEmptyStringsToNull.php:27
51 - vendor\laravel\framework\src\Illuminate\Pipeline\Pipeline.php:219
52 - vendor\laravel\framework\src\Illuminate\Foundation\Http\Middleware\TrimStrings.php:47
53 - vendor\laravel\framework\src\Illuminate\Pipeline\Pipeline.php:219
54 - vendor\laravel\framework\src\Illuminate\Http\Middleware\ValidatePostSize.php:27
55 - vendor\laravel\framework\src\Illuminate\Pipeline\Pipeline.php:219
56 - vendor\laravel\framework\src\Illuminate\Foundation\Http\Middleware\PreventRequestsDuringMaintenance.php:109
57 - vendor\laravel\framework\src\Illuminate\Pipeline\Pipeline.php:219
58 - vendor\laravel\framework\src\Illuminate\Http\Middleware\HandleCors.php:61
59 - vendor\laravel\framework\src\Illuminate\Pipeline\Pipeline.php:219
60 - vendor\laravel\framework\src\Illuminate\Http\Middleware\TrustProxies.php:58
61 - vendor\laravel\framework\src\Illuminate\Pipeline\Pipeline.php:219
62 - vendor\laravel\framework\src\Illuminate\Foundation\Http\Middleware\InvokeDeferredCallbacks.php:22
63 - vendor\laravel\framework\src\Illuminate\Pipeline\Pipeline.php:219
64 - vendor\laravel\framework\src\Illuminate\Http\Middleware\ValidatePathEncoding.php:28
65 - vendor\laravel\framework\src\Illuminate\Pipeline\Pipeline.php:219
66 - vendor\laravel\framework\src\Illuminate\Pipeline\Pipeline.php:137
67 - vendor\laravel\framework\src\Illuminate\Foundation\Http\Kernel.php:175
68 - vendor\laravel\framework\src\Illuminate\Foundation\Http\Kernel.php:144
69 - vendor\laravel\framework\src\Illuminate\Foundation\Application.php:1220
70 - public\index.php:20

## Previous exception

### 1. PDOException

SQLSTATE[23000]: Integrity constraint violation: 19 NOT NULL constraint failed: siswas.kelas

0 - vendor\laravel\framework\src\Illuminate\Database\Connection.php:587
1 - vendor\laravel\framework\src\Illuminate\Database\Connection.php:587
2 - vendor\laravel\framework\src\Illuminate\Database\Connection.php:830
3 - vendor\laravel\framework\src\Illuminate\Database\Connection.php:797
4 - vendor\laravel\framework\src\Illuminate\Database\Connection.php:576
5 - vendor\laravel\framework\src\Illuminate\Database\Connection.php:540
6 - vendor\laravel\framework\src\Illuminate\Database\Query\Processors\Processor.php:32
7 - vendor\laravel\framework\src\Illuminate\Database\Query\Builder.php:4251
8 - vendor\laravel\framework\src\Illuminate\Database\Eloquent\Builder.php:2271
9 - vendor\laravel\framework\src\Illuminate\Database\Eloquent\Model.php:1660
10 - vendor\laravel\framework\src\Illuminate\Database\Eloquent\Model.php:1576
11 - vendor\laravel\framework\src\Illuminate\Database\Eloquent\Model.php:1380
12 - vendor\filament\filament\src\Resources\Pages\CreateRecord.php:221
13 - vendor\filament\filament\src\Resources\Pages\CreateRecord.php:113
14 - vendor\laravel\framework\src\Illuminate\Container\BoundMethod.php:36
15 - vendor\laravel\framework\src\Illuminate\Container\Util.php:43
16 - vendor\laravel\framework\src\Illuminate\Container\BoundMethod.php:96
17 - vendor\laravel\framework\src\Illuminate\Container\BoundMethod.php:35
18 - vendor\livewire\livewire\src\Wrapped.php:23
19 - vendor\livewire\livewire\src\Mechanisms\HandleComponents\HandleComponents.php:697
20 - vendor\livewire\livewire\src\Mechanisms\HandleComponents\HandleComponents.php:240
21 - vendor\livewire\livewire\src\LivewireManager.php:131
22 - vendor\livewire\livewire\src\Mechanisms\HandleRequests\HandleRequests.php:202
23 - vendor\laravel\framework\src\Illuminate\Routing\ControllerDispatcher.php:46
24 - vendor\laravel\framework\src\Illuminate\Routing\Route.php:269
25 - vendor\laravel\framework\src\Illuminate\Routing\Route.php:215
26 - vendor\laravel\framework\src\Illuminate\Routing\Router.php:822
27 - vendor\laravel\framework\src\Illuminate\Pipeline\Pipeline.php:180
28 - vendor\livewire\livewire\src\Mechanisms\HandleRequests\RequireLivewireHeaders.php:19
29 - vendor\laravel\framework\src\Illuminate\Pipeline\Pipeline.php:219
30 - vendor\laravel\framework\src\Illuminate\Routing\Middleware\SubstituteBindings.php:52
31 - vendor\laravel\framework\src\Illuminate\Pipeline\Pipeline.php:219
32 - vendor\laravel\framework\src\Illuminate\Foundation\Http\Middleware\PreventRequestForgery.php:104
33 - vendor\laravel\framework\src\Illuminate\Pipeline\Pipeline.php:219
34 - vendor\laravel\framework\src\Illuminate\View\Middleware\ShareErrorsFromSession.php:48
35 - vendor\laravel\framework\src\Illuminate\Pipeline\Pipeline.php:219
36 - vendor\laravel\framework\src\Illuminate\Session\Middleware\StartSession.php:120
37 - vendor\laravel\framework\src\Illuminate\Session\Middleware\StartSession.php:63
38 - vendor\laravel\framework\src\Illuminate\Pipeline\Pipeline.php:219
39 - vendor\laravel\framework\src\Illuminate\Cookie\Middleware\AddQueuedCookiesToResponse.php:36
40 - vendor\laravel\framework\src\Illuminate\Pipeline\Pipeline.php:219
41 - vendor\laravel\framework\src\Illuminate\Cookie\Middleware\EncryptCookies.php:74
42 - vendor\laravel\framework\src\Illuminate\Pipeline\Pipeline.php:219
43 - vendor\laravel\framework\src\Illuminate\Pipeline\Pipeline.php:137
44 - vendor\laravel\framework\src\Illuminate\Routing\Router.php:821
45 - vendor\laravel\framework\src\Illuminate\Routing\Router.php:800
46 - vendor\laravel\framework\src\Illuminate\Routing\Router.php:764
47 - vendor\laravel\framework\src\Illuminate\Routing\Router.php:753
48 - vendor\laravel\framework\src\Illuminate\Foundation\Http\Kernel.php:200
49 - vendor\laravel\framework\src\Illuminate\Pipeline\Pipeline.php:180
50 - vendor\livewire\livewire\src\Features\SupportDisablingBackButtonCache\DisableBackButtonCacheMiddleware.php:19
51 - vendor\laravel\framework\src\Illuminate\Pipeline\Pipeline.php:219
52 - vendor\laravel\framework\src\Illuminate\Foundation\Http\Middleware\ConvertEmptyStringsToNull.php:27
53 - vendor\laravel\framework\src\Illuminate\Pipeline\Pipeline.php:219
54 - vendor\laravel\framework\src\Illuminate\Foundation\Http\Middleware\TrimStrings.php:47
55 - vendor\laravel\framework\src\Illuminate\Pipeline\Pipeline.php:219
56 - vendor\laravel\framework\src\Illuminate\Http\Middleware\ValidatePostSize.php:27
57 - vendor\laravel\framework\src\Illuminate\Pipeline\Pipeline.php:219
58 - vendor\laravel\framework\src\Illuminate\Foundation\Http\Middleware\PreventRequestsDuringMaintenance.php:109
59 - vendor\laravel\framework\src\Illuminate\Pipeline\Pipeline.php:219
60 - vendor\laravel\framework\src\Illuminate\Http\Middleware\HandleCors.php:61
61 - vendor\laravel\framework\src\Illuminate\Pipeline\Pipeline.php:219
62 - vendor\laravel\framework\src\Illuminate\Http\Middleware\TrustProxies.php:58
63 - vendor\laravel\framework\src\Illuminate\Pipeline\Pipeline.php:219
64 - vendor\laravel\framework\src\Illuminate\Foundation\Http\Middleware\InvokeDeferredCallbacks.php:22
65 - vendor\laravel\framework\src\Illuminate\Pipeline\Pipeline.php:219
66 - vendor\laravel\framework\src\Illuminate\Http\Middleware\ValidatePathEncoding.php:28
67 - vendor\laravel\framework\src\Illuminate\Pipeline\Pipeline.php:219
68 - vendor\laravel\framework\src\Illuminate\Pipeline\Pipeline.php:137
69 - vendor\laravel\framework\src\Illuminate\Foundation\Http\Kernel.php:175
70 - vendor\laravel\framework\src\Illuminate\Foundation\Http\Kernel.php:144
71 - vendor\laravel\framework\src\Illuminate\Foundation\Application.php:1220
72 - public\index.php:20

## Request

POST /livewire-6c501099/update

## Headers

* **cookie**: XSRF-TOKEN=eyJpdiI6IkJOSEtHQ1plcE1yVXdkQjhJSENNbEE9PSIsInZhbHVlIjoiQldPN0kzVG0rdFZ2Sk94K1ZSTGI2VnB5YWhFNnhmd1Q4Z2JCc0RnWDNYZXlzR0NDTTNtMWRJeGZ6YksxV0t5a2dlTk1INHd3VUg4R3FDK05xN0h0YWVkakFja3dVVXFybVZZaW0xUXZjcnhLZDNMRFIzOVJyVnBLdHZzbTdwMGwiLCJtYWMiOiI5YzRiY2E5YWJhNmMxY2ZhOGIxMzA3NzU1ZjI1NzFlYjIxZjFjMWYyMGUzMWM1ZTMyZmZkNjMwZjJmODU1MGFmIiwidGFnIjoiIn0%3D; laravel-session=eyJpdiI6Ik00dG9Ya3BRWVNRb0tBVkFsYWM1dmc9PSIsInZhbHVlIjoiUlZkdXNIa1NVb010azg5UCt5MDA1cXpoYlQxd0NjVldjY3h6dWdRQ0kzNWpOMGdkeUV6cHlPRmRGaGlQekUwZ2xNM3pGTDI0S0wrSy9SV0FuTDlKQ1RoQUNBQkd4OThSUkVHWitKUnh6RVU2RVBzZTIxVUdTYmRUSjhlZmpENFEiLCJtYWMiOiJiZTM0ZTliMTlhMGE3NzU5Y2E0MzAxYzViZTA0YTY4Yzg3MGQxODM4YmY5ZTZiN2YxOGYyODcyZjA0MDYzZjA4IiwidGFnIjoiIn0%3D
* **accept-language**: en-GB,en-US;q=0.9,en;q=0.8,id;q=0.7
* **accept-encoding**: gzip, deflate
* **referer**: http://website-absensi-mm2.test:8080/admin/siswas/create
* **origin**: http://website-absensi-mm2.test:8080
* **accept**: */*
* **x-livewire**: 1
* **content-type**: application/json
* **user-agent**: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/149.0.0.0 Safari/537.36
* **content-length**: 1272
* **connection**: keep-alive
* **host**: website-absensi-mm2.test:8080

## Route Context

controller: Livewire\Mechanisms\HandleRequests\HandleRequests@handleUpdate
route name: default-livewire.update
middleware: web, Livewire\Mechanisms\HandleRequests\RequireLivewireHeaders

## Route Parameters

No route parameter data available.

## Database Queries

* sqlite - select * from "sessions" where "id" = 'YNscwWB7EK1PUghBvaTk4m86NA3kznFC3lb36H1I' limit 1 (3.45 ms)
* sqlite - select * from "cache" where "key" in ('laravel-cache-livewire-checksum-failures:127.0.0.1') (0.23 ms)
* sqlite - select * from "users" where "id" = 1 limit 1 (0.2 ms)
* sqlite - select count(*) as "aggregate" from "siswas" where "nisn" = '57438573498573495734175197' (0.29 ms)

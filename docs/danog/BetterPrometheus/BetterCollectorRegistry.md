---
title: "danog\\BetterPrometheus\\BetterCollectorRegistry: A better collector registry."
description: ""

---
# `danog\BetterPrometheus\BetterCollectorRegistry`
[Back to index](../../index.md)

> Author: Daniil Gentili <daniil@daniil.it>  
  

A better collector registry.  



## Properties
* `$storageAdapter`: `Prometheus\Storage\Adapter` 

## Method list:
* [`__construct(\Prometheus\Storage\Adapter $storageAdapter, bool $registerDefaultMetrics = true)`](#__construct)
* [`wipeStorage(): void`](#wipeStorage)
* [`getMetricFamilySamples(bool $sortMetrics = true): list<\Prometheus\MetricFamilySamples>`](#getMetricFamilySamples)
* [`registerGauge(string $namespace, string $name, string $help, array<string, string> $labels = []): \danog\BetterPrometheus\BetterGauge`](#registerGauge)
* [`getGauge(string $namespace, string $name): \danog\BetterPrometheus\BetterGauge`](#getGauge)
* [`getOrRegisterGauge(string $namespace, string $name, string $help, array<string, string> $labels = []): \danog\BetterPrometheus\BetterGauge`](#getOrRegisterGauge)
* [`registerCounter(string $namespace, string $name, string $help, array<string, string> $labels = []): \danog\BetterPrometheus\BetterCounter`](#registerCounter)
* [`getCounter(string $namespace, string $name): \danog\BetterPrometheus\BetterCounter`](#getCounter)
* [`getOrRegisterCounter(string $namespace, string $name, string $help, array<string, string> $labels = []): \danog\BetterPrometheus\BetterCounter`](#getOrRegisterCounter)
* [`registerHistogram(string $namespace, string $name, string $help, array<string, string> $labels = [], (non-empty-list<float>|null) $buckets = NULL): \danog\BetterPrometheus\BetterHistogram`](#registerHistogram)
* [`getHistogram(string $namespace, string $name): \danog\BetterPrometheus\BetterHistogram`](#getHistogram)
* [`getOrRegisterHistogram(string $namespace, string $name, string $help, array<string, string> $labels = [], (non-empty-list<float>|null) $buckets = NULL): \danog\BetterPrometheus\BetterHistogram`](#getOrRegisterHistogram)
* [`registerSummary(string $namespace, string $name, string $help, array<string, string> $labels = [], int $maxAgeSeconds = 600, (non-empty-list<float>|null) $quantiles = NULL): \danog\BetterPrometheus\BetterSummary`](#registerSummary)
* [`getSummary(string $namespace, string $name): \danog\BetterPrometheus\BetterSummary`](#getSummary)
* [`getOrRegisterSummary(string $namespace, string $name, string $help, array<string, string> $labels = [], int $maxAgeSeconds = 600, (non-empty-list<float>|null) $quantiles = NULL): \danog\BetterPrometheus\BetterSummary`](#getOrRegisterSummary)

## Methods:
### <a name="__construct"></a> `__construct(\Prometheus\Storage\Adapter $storageAdapter, bool $registerDefaultMetrics = true)`

CollectorRegistry constructor.


Parameters:

* `$storageAdapter`: `\Prometheus\Storage\Adapter`   
* `$registerDefaultMetrics`: `bool`   


#### See also: 
* `\Prometheus\Storage\Adapter`




### <a name="wipeStorage"></a> `wipeStorage(): void`

Removes all previously stored metrics from underlying storage adapter.



### <a name="getMetricFamilySamples"></a> `getMetricFamilySamples(bool $sortMetrics = true): list<\Prometheus\MetricFamilySamples>`




Parameters:

* `$sortMetrics`: `bool`   


#### See also: 
* `\Prometheus\MetricFamilySamples`




### <a name="registerGauge"></a> `registerGauge(string $namespace, string $name, string $help, array<string, string> $labels = []): \danog\BetterPrometheus\BetterGauge`




Parameters:

* `$namespace`: `string` e.g. cms  
* `$name`: `string` e.g. duration_seconds  
* `$help`: `string` e.g. The duration something took in seconds.  
* `$labels`: `array<string, string>` e.g. ['controller' => 'someController', 'action' => 'someAction']  


#### See also: 
* [`\danog\BetterPrometheus\BetterGauge`: A better prometheus gauge.](../../danog/BetterPrometheus/BetterGauge.md)




### <a name="getGauge"></a> `getGauge(string $namespace, string $name): \danog\BetterPrometheus\BetterGauge`




Parameters:

* `$namespace`: `string`   
* `$name`: `string`   


#### See also: 
* [`\danog\BetterPrometheus\BetterGauge`: A better prometheus gauge.](../../danog/BetterPrometheus/BetterGauge.md)




### <a name="getOrRegisterGauge"></a> `getOrRegisterGauge(string $namespace, string $name, string $help, array<string, string> $labels = []): \danog\BetterPrometheus\BetterGauge`




Parameters:

* `$namespace`: `string` e.g. cms  
* `$name`: `string` e.g. duration_seconds  
* `$help`: `string` e.g. The duration something took in seconds.  
* `$labels`: `array<string, string>` e.g. ['controller' => 'someController', 'action' => 'someAction']  


#### See also: 
* [`\danog\BetterPrometheus\BetterGauge`: A better prometheus gauge.](../../danog/BetterPrometheus/BetterGauge.md)




### <a name="registerCounter"></a> `registerCounter(string $namespace, string $name, string $help, array<string, string> $labels = []): \danog\BetterPrometheus\BetterCounter`




Parameters:

* `$namespace`: `string` e.g. cms  
* `$name`: `string` e.g. requests  
* `$help`: `string` e.g. The number of requests made.  
* `$labels`: `array<string, string>` e.g. ['controller' => 'someController', 'action' => 'someAction']  


#### See also: 
* [`\danog\BetterPrometheus\BetterCounter`: A better prometheus counter.](../../danog/BetterPrometheus/BetterCounter.md)




### <a name="getCounter"></a> `getCounter(string $namespace, string $name): \danog\BetterPrometheus\BetterCounter`




Parameters:

* `$namespace`: `string`   
* `$name`: `string`   


#### See also: 
* [`\danog\BetterPrometheus\BetterCounter`: A better prometheus counter.](../../danog/BetterPrometheus/BetterCounter.md)




### <a name="getOrRegisterCounter"></a> `getOrRegisterCounter(string $namespace, string $name, string $help, array<string, string> $labels = []): \danog\BetterPrometheus\BetterCounter`




Parameters:

* `$namespace`: `string` e.g. cms  
* `$name`: `string` e.g. requests  
* `$help`: `string` e.g. The number of requests made.  
* `$labels`: `array<string, string>` e.g. ['controller' => 'someController', 'action' => 'someAction']  


#### See also: 
* [`\danog\BetterPrometheus\BetterCounter`: A better prometheus counter.](../../danog/BetterPrometheus/BetterCounter.md)




### <a name="registerHistogram"></a> `registerHistogram(string $namespace, string $name, string $help, array<string, string> $labels = [], (non-empty-list<float>|null) $buckets = NULL): \danog\BetterPrometheus\BetterHistogram`




Parameters:

* `$namespace`: `string` e.g. cms  
* `$name`: `string` e.g. duration_seconds  
* `$help`: `string` e.g. A histogram of the duration in seconds.  
* `$labels`: `array<string, string>` e.g. ['controller' => 'someController', 'action' => 'someAction']  
* `$buckets`: `(non-empty-list<float>|null)` e.g. [100, 200, 300]  


#### See also: 
* `non-empty-list`
* [`\danog\BetterPrometheus\BetterHistogram`: A better prometheus histogram.](../../danog/BetterPrometheus/BetterHistogram.md)




### <a name="getHistogram"></a> `getHistogram(string $namespace, string $name): \danog\BetterPrometheus\BetterHistogram`




Parameters:

* `$namespace`: `string`   
* `$name`: `string`   


#### See also: 
* [`\danog\BetterPrometheus\BetterHistogram`: A better prometheus histogram.](../../danog/BetterPrometheus/BetterHistogram.md)




### <a name="getOrRegisterHistogram"></a> `getOrRegisterHistogram(string $namespace, string $name, string $help, array<string, string> $labels = [], (non-empty-list<float>|null) $buckets = NULL): \danog\BetterPrometheus\BetterHistogram`




Parameters:

* `$namespace`: `string` e.g. cms  
* `$name`: `string` e.g. duration_seconds  
* `$help`: `string` e.g. A histogram of the duration in seconds.  
* `$labels`: `array<string, string>` e.g. ['controller' => 'someController', 'action' => 'someAction']  
* `$buckets`: `(non-empty-list<float>|null)` e.g. [100, 200, 300]  


#### See also: 
* `non-empty-list`
* [`\danog\BetterPrometheus\BetterHistogram`: A better prometheus histogram.](../../danog/BetterPrometheus/BetterHistogram.md)




### <a name="registerSummary"></a> `registerSummary(string $namespace, string $name, string $help, array<string, string> $labels = [], int $maxAgeSeconds = 600, (non-empty-list<float>|null) $quantiles = NULL): \danog\BetterPrometheus\BetterSummary`




Parameters:

* `$namespace`: `string` e.g. cms  
* `$name`: `string` e.g. duration_seconds  
* `$help`: `string` e.g. A summary of the duration in seconds.  
* `$labels`: `array<string, string>` e.g. ['controller' => 'someController', 'action' => 'someAction']  
* `$maxAgeSeconds`: `int` e.g. 604800  
* `$quantiles`: `(non-empty-list<float>|null)` e.g. [0.01, 0.5, 0.99]  


#### See also: 
* `non-empty-list`
* [`\danog\BetterPrometheus\BetterSummary`: A better prometheus summary.](../../danog/BetterPrometheus/BetterSummary.md)




### <a name="getSummary"></a> `getSummary(string $namespace, string $name): \danog\BetterPrometheus\BetterSummary`




Parameters:

* `$namespace`: `string`   
* `$name`: `string`   


#### See also: 
* [`\danog\BetterPrometheus\BetterSummary`: A better prometheus summary.](../../danog/BetterPrometheus/BetterSummary.md)




### <a name="getOrRegisterSummary"></a> `getOrRegisterSummary(string $namespace, string $name, string $help, array<string, string> $labels = [], int $maxAgeSeconds = 600, (non-empty-list<float>|null) $quantiles = NULL): \danog\BetterPrometheus\BetterSummary`




Parameters:

* `$namespace`: `string` e.g. cms  
* `$name`: `string` e.g. duration_seconds  
* `$help`: `string` e.g. A summary of the duration in seconds.  
* `$labels`: `array<string, string>` e.g. ['controller' => 'someController', 'action' => 'someAction']  
* `$maxAgeSeconds`: `int` e.g. 604800  
* `$quantiles`: `(non-empty-list<float>|null)` e.g. [0.01, 0.5, 0.99]  


#### See also: 
* `non-empty-list`
* [`\danog\BetterPrometheus\BetterSummary`: A better prometheus summary.](../../danog/BetterPrometheus/BetterSummary.md)




---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

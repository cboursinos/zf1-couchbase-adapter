# zf1-couchbase-adapter
ZF1 Couchbase Adapter

# How to use it

```
if (!Zend_Registry::isRegistered('cache')) {
			$config = Zend_Registry::get('config')->cache;
			$backendOptions = $config->backendOptions->toArray();

			$flightSearchCache = Zend_Cache::factory(
				'Core', $config->backend, ['automatic_serialization' => true, 'write_control' => false], $backendOptions, true
			);
			Zend_Registry::set('cache', $flightSearchCache);
		}
		return Zend_Registry::get('cache');

```

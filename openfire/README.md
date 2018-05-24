# Openfire Custom Configuration
provider.auth.className=org.jivesoftware.openfire.auth.HybridAuthProvider
hybridAuthProvider.primaryProvider.className=org.jivesoftware.openfire.auth.[TDAUX_CUSTOM_AUTH]
hybridAuthProvider.secondaryProvider.className=org.jivesoftware.openfire.auth.DefaultAuthProvider

tdaux.infinispan.host = [DATA_GRID_HOST].default.svc.cluster.local
tdaux.infinispan.port = [DATA_GRID_PORT]


tdaux.coreservice.dmsmap = http://[CORE_API]:[PORT]/core-service/api/tcloud/v1
tdaux.coreservice.documetaccess = http://[CORE_API]:[PORT]/core-service/api/security/v1
tdaux.coreservice.message = http://[CORE_API]:[PORT]/core-service/api/bms/rooms/v1

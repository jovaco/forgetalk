# forgetalk
# **Command line used to build the project :**

`project-new --named forgetalk
jpa-new-entity --named Book
jpa-new-field --named title
jpa-new-field --named isbn
jpa-new-field --named price --type java.lang.Float
jpa-new-field --named discount --type java.lang.Float --transient

scaffold-generate --provider Faces --targets  org.forgetalk.model.*
rest-generate-endpoints-from-entities --targets org.forgetalk.model.*


rhc app create forgetalke jboss-wildfly-10 --from-code https://github.com/jovaco/forgetalke.git`

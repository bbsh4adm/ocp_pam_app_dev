FROM scratch

LABEL   maintainer="rromerom@redhat.com" \
        name="Oracle JDBC Driver" \
        version="12.1.0.1"

# Provide the right value during build
ARG ARTIFACT_MVN_REPO

COPY install.sh oracle-driver-image/install.properties /extensions/
COPY oracle-driver-image/modules /extensions/modules/

# Download the driver into the module folder
#ADD ${ARTIFACT_MVN_REPO}/com/oracle/ojdbc7/12.1.0.1/ojdbc7-12.1.0.1.jar \
#    /extensions/modules/system/layers/openshift/com/oracle/main/ojdbc7.jar

# COPY Driver from local location into the image location (if driver locally available rather than in remote repository)
COPY oracle-driver-image/ojdbc7-12.1.0.1.jar /extensions/modules/system/layers/openshift/com/oracle/main/ojdbc7.jar


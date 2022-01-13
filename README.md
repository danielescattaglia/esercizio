**ESERCIZIO 1**
- Creazione di un cluster Kubernetes. Nel cluster deve essere anche presente il registro per le immagini docker. Qualsiasi configurazione va bene, 
  posso avere anche un solo nodo.


    https://minikube.sigs.k8s.io/docs/
    https://minikube.sigs.k8s.io/docs/handbook/registry/

**ESERCIZIO 2**
- Creazione di un'immagine docker che erediti da nginx e che contenga al suo interno una pagina html statica. All'interno dell'immagine deve esistere anche 
  la configurazione per un virtual host esercizio.exmitalia.it
  
  
    https://www.nginx.com/resources/wiki/start/topics/examples/server_blocks/

**ESERCIZIO 3**
- Creazione dei Dockerfile per i nodi Ethereum con geth (uno con funzionalità di mining e uno senza) e della relativa immagin. Inserire poi l'immagine creata nel registro del cluster. 
  Creare un pod che utilizzi l'immagine creata. Il pod deve rimare Running per 5000 secondi (sleep 5000)


    https://docs.docker.com/engine/reference/builder/
    https://minikube.sigs.k8s.io/docs/handbook/pushing/

**ESERCIZIO 4**
- Creazione di una rete privata Ethereum all'interno del cluster utilizzando le immagini create in precedenza. La rete deve avere un nodo pubblico ed uno privato.
   Il meccanismo di discovery di geth deve essere disabilitato. La rete deve avere id 1234567. Una volta attivi i pod:
   - mettere in comunicazione i due nodi in maniera statica. Recuperare gli indirizzi ip dei pod attraverso il meccanismo dei servizi e del DNS di K8s. Salvare il
      risultato di admin.peers
   
    
    https://kubernetes.io/docs/tasks/debug-application-cluster/get-shell-running-container/
    https://kubernetes.io/docs/concepts/services-networking/dns-pod-service/
    https://kubernetes.io/docs/concepts/services-networking/service/#headless-services
    https://geth.ethereum.org/docs/interface/peer-to-peer
    https://kubernetes.io/docs/tutorials/stateful-application/basic-stateful-set/

**ESERCIZIO 5**
- Creazione su kubernetes dello storage persistente per la directory in cui geth salva il database.
 
 
    https://kubernetes.io/docs/concepts/storage/persistent-volumes/
    
**ESERCIZIO 6**
- Completato l'esercizio 4, creare uno script che metta in comunicazione i due nodi geth in maniera automatica. Deve essere gestito il caso in cui i pod 
  cambino indirizzo ip. All'interno dello script devono esserci le istruzioni per il salvataggio dei log su file.

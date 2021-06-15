# Project2021DDPMS

Ανάπτυξη Εφαρμογής για εκτέλεση αναζητήσεων στο περιβάλλον του Elasticsearch

# Εισαγωγή

To Elasticsearch, είναι μια μηχανή αναζήτησης πραγματικού χρόνου (Real time search) και ανάλυσης δεδομένων (analytics engine). Βασίζεται στο apache lucene1, μια υψηλών επιδόσεων με αρκετά χαρακτηριστικά βιβλιοθήκη για μηχανές αναζήτησης.

Τα Elasticsearch είναι:

#### • Distributed: μπορεί να «τρέχει» σε ξεχωριστούς server (clustering) κατανέμοντας τον όγκο των πληροφοριών σε διαφορετικούς κόμβους

#### • Scalable: το σύστημα καθορίζει αυτόματα την εκχώρηση των τμημάτων (shards) σε κάθε κόμβο που προστίθενται στο cluster

#### • High availability: Σε περίπτωση που κάποιος κόμβος αποκοπεί από το cluster, τα δεδομένα μετατίθενται αυτόματα στους υπόλοιπους

#### • REST API: όλες οι λειτουργίες γίνονται βάση της αρχιτεκτονικής REST, από την δημιουργία των indices έως τον έλεγχο του αριθμού των αντιγράφων ανά index, προσδίδοντας ευελιξία στην ανάπτυξη γρήγορου κώδικα (rapid development)

#### • JSON over HTTP: τα αιτήματα(requests) και οι απαντήσεις(responses) για την ανάκτηση των δεδομένων γίνονται xχρησιμοποιώντας δομές JSON, κάνοντας ευκολότερη την ανάγνωση του κώδικα

#### • Είναι ανοιχτού κώδικα

#### • Είναι Multi tenancy

Το Elastic Stack (ELK stack) είναι ο συνδυασμός τριών διαφορετικών τεχνολογιών: Elasticsearch, Logstash και Kibana. Το Logstash είναι ένας αγωγός επεξεργασίας δεδομένων (pipeline) από τα σημεία ενδιαφέροντος και από πολλές πηγές ταυτόχρονα, τα μετατρέπει και, στη συνέχεια, τα στέλνει σε ένα "stash" όπως το Elasticsearch. Το Kibana επιτρέπει στους χρήστες να οπτικοποιούν δεδομένα με γραφήματα και γραφήματα στο Elasticsearch.

# Σκοπός/Στόχος της εργασίας

Σκοπός της εργασίας είναι να περιγράφει και να δημιουργηθεί δικτυακή εφαρμογή (με ύπαρξη σχετικού UI) με σκοπό την εκτέλεση αναζητήσεων στην μηχανή του Elasticsearch και την παρουσίαση των σχετικών αποτελεσμάτων αυτών. Για τη δημιουργία της εν λόγω εφαρμογής προτείνεται η γλώσσα Java με υποστήριξη από frameworks όπως Maven 2και Spring Boot.

Στόχος της εργασίας είναι να παρουσιαστούν όλες οι πλευρές/δυσκολίες/ανησυχίες τόσο αναφορικά με την ανάπτυξη της εφαρμογής όσο και με το "στήσιμο" του περιβάλλοντος του ELK. Ιδιαίτερη έμφαση θα δοθεί στην ασφαλή λειτουργία του ELK με τη χρήση του πρωτοκόλλου TLS. Για την ανάπτυξη της εφαρμογής σας θα σας δοθεί ένα template project το οποίο θα περιλαμβάνει έτοιμο το functionality αναφορικά με τη σύνδεση με το REST API του Elasticsearch

# Απαιτήσεις

1. Λειτουργικό Σύστημα Linux (native/VM) 18.04 LTS Server (Minimum 4GB RAM, 1~2 Cores, 50GB HD)
2. openjdk version 1.8 ή openjdk version 11 (για debug). Για την εγκατάσταση του εκτελέστε στο terminal του vm σας το εξής:

    ```console
     sudo apt-get install openjdk-11-jdk 
    ```

3. OpenJDK Runtime Environment. Για την εγκατάσταση του εκτελέστε στο terminal του vm σας το εξής:  

    ```console
     sudo apt install default-jre
    ```

4. Maven (latest version). Για την εγκατάσταση του εκτελέστε στο terminal του vm σας το εξής:  

    ```console
      sudo apt install maven
    ```

      Μετά την εγκατάσταση του Maven βεβαιωθείτε για την έκδοση του με τον εξής τρόπο

    ```console
      mvn -version
    ```

      Δείτε περισσότερα επίσης στα κάτωθι links αναφορικά με το Maven

<https://linuxize.com/post/how-to-install-apache-maven-on-ubuntu-18-04/>

<https://maven.apache.org/install.html>

<https://www.baeldung.com/install-maven-on-windows-linux-mac>

# Download dependencies και compile (under Maven)

Μεταβείτε στον root φάκελο του Project και εκτελέστε διαδοχικά
    ```console
      mvn -version
    ```

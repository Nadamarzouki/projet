# projet 
typedef struct{ 
    int jour ;
    int mois ;
    int annee;
} Date;
typedef struct
{
    int id_fiche; 
    char CIN[20]; 
    Date Date_de_RDV; 
    char ETS[50]; 
    char Creneau[20]; 
    char Groupe_sanguin[5]; 
    char Habitude[30]; 
} Fiche;


typedef struct{
    char id[20];
    char cin[20];
    char region[20];
    char nom_etablissement[20];
    Date date_rdv;
    char creneau[20];
} rdv;
typedef struct {
    char id[20];
    char nom[50];
    char adresse_etab[50];
    int classification;
    char region[50];
    int capacite;
    int service[5];
    char num_tel[50];
    char email[50];
} etab;
int ajouter_fiche(char *filename, Fiche Fi);
int modifier_fiche( char *filename, int id, Fiche nouv);
int supprimer_fiche(char *filename, int id);
Fiche chercher_fiche(char *filename, int id);
void afficher_fiche(GtkWidget *liste, char *filename);
void afficher_rdv(GtkWidget *liste, char file[20]);
int nbETS(char nomFichier[]);
float moyRDV_ETS(char nomFichier[], int jour, int mois, int annee);
int listeRDV(char nomfichier[], char etablissement[], int jour, int mois, int annee);


#endif // FUNCTION_H_INCLUDED

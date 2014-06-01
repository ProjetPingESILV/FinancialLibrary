FinancialLibrary
================

Librairie Financière (ensemble de fonctions concernant le pricing d'une option)


I)	Modèle de Pricing
   
    1)	Modèle Binomial
      
      Fonction qui renvoie l'arbre de départ utilisé pour calculer le prix : 
      public static double[,] arbreDuStock(double s, double u, double d, int n)
     
      Details des paramètres : 
      s : Prix spot a l'instant initial 
      u : Le up factor
      d : Le down factor,
      n : Le nombre de periodes 
      Fonction qui affiche l'arbre des prix
      
      public static double[,] ArbrePrix(string callput,string type,double s,double u,double d,double k,double r,int n)
      
      Details des paramètres : 
      callput : Call ou put
      type Le type americain ou europeen,
      s : Prix spot à l'instant initial
      u : Le up factor double u
      d : Le down factor double d
      k : Le strike
      r : Le taux sans risque,
      n : Le nombre de periodes 
      Fonction qui permet de calculer le prix d'une option avec l'arbre binomial

      Fonction qui calcule le prix d'une option
        public static double CalculPrixOption(string callput,string type,double s,double u,double d,double k,double r,int       n)
      Details des paramètres : 

      callput : Call ou put
      type : Le type americain ou europeen,
      s : Prix spot à l'instant initial,
      u : Le up factor  u
      d : Le down factor d,
      k : Le strike 
      r : Le taux sans risque 
      n : Le nombre de periodes 

    
    2)	Modèle Black-Scholes
      
      Fonction qui calcule le prix d'une option avec la formule de Black et Scholes
        public static double blackScholes(string callput,string type,double s,double sigma,double t,double taux,double       strike)
      
      Details des paramètres : 
      Call ou put callput,
      type : Le type americain ou europeen 
      s : Le prix spot a l'instant initial
      sigma : La volatilite de l'action 
      t : La maturite en annees
      taux : Le taux sans risque
      strike : Le strike price 
    
    
    
    3)	Formule de Cox Rox Rubinstein
      
      Fonction qui calcule le prix d'une option à partir des formules de Cox Rox Rubinstein : 
        public static double PrixCrr(string callput,string type,double s,double sigma,double t,double taux,double strike)
      
      Details des paramètres : 
      callput : Call ou put
      type : Le type americain ou europeen 
      s : Le prix spot a l'instant initial
      sigma : La volatilite de l'action 
      t : La maturite en annees
      taux : Le taux sans risque
      strike : Le strike price
  
  
  
  II)	Greeks
      Delta : sensibilité du prix d’une option à un mouvement du prix du sousjacent.
      Public double Delta_BlackScholes_Call(T, r, sigma, S0, K, t, s)
      Public double Delta_BlackScholes_Put(T, r, sigma, S0, K, t, s)
      Gamma : sensibilité du deuxième ordre à un mouvement du prix du sousjacent.
         Public double Gamma_BlackScholes (T, r, sigma, S0, K, t, s)
      heta : sensibilité du prix de l’option par rapport au temps.
      Public double Theta_BlackScholes_Call(T, r, sigma, S0, K, t, s)
      Public double Theta_BlackScholes_Put(T, r, sigma, S0, K, t, s)
      Rho : sensibilité du prix d’une option à unmouvement des taux d’intérêts
      Public double Rho_BlackScholes_Call(T, r, sigma, S0, K, t, s)
      Public double Rho_BlackScholes_Put(T, r, sigma, S0, K, t, s)
      Vega : sensibilité du prix d’une option à un mouvement au niveau de la volatilité du sous-jacent
      Public double Vega_BlackScholes (T, r, sigma, S0, K, t, s)

	      T : maturité
	      K : strike
         sigma : volatilité
         r : taux sans risque
      	S0 : prix spot a l'instant initial


## No predictor model
$y_i \sim Bern(\theta_i)$   
$logit(\theta_i) = \beta_0$   

## 2 predictor model
$y_i \sim Bern(\theta_i)$   
$logit(\theta_i) = \beta_0 + \beta_1 e_i + \beta_2 c_i$   

## All predictor model (using default priors)
$y_i \sim Bern(\theta_i)$   
$logit(\theta_i) = \beta_0 + \beta_1 a_i + \beta_2 m_i + \beta_3 h_i + \beta_4 k_i + \beta_5 d_i + \beta_6 e_i + \beta_7 p_i + \beta_8 x_i + \beta_9 c_i + \beta_{10} s_i + \beta_{11} g_i$   

## Horseshoe   
$y_i \sim Bern(\theta_i)$   
$logit(\theta_i) = \beta_0 + \beta_1 a_i + \beta_2 m_i + \beta_3 h_i + \beta_4 k_i + \beta_5 d_i + \beta_6 e_i + \beta_7 p_i + \beta_8 x_i + \beta_9 c_i + \beta_{10} s_i + \beta_{11} g_i$   
$\beta_0 \sim N(0, 1)$   
$\beta_j | \lambda_j, \tau \sim N(0, \lambda_j \tau)$   
$\lambda_j \sim C^+(0, 1)$, $j=1, \cdots, P$   
$\tau \sim C^+(0, \tau_0)$ where $\tau_0 = \frac{p_0}{P-p_0} \frac{\sigma}{\sqrt{n}}$   
We approximate $\sigma$ with pseudo variance $\tilde{\sigma}^2=1/\mu(1-\mu)$ for non-gaussian link  

## Regularized Horseshoe   
$y_i \sim Bern(\theta_i)$   
$logit(\theta_i) = \beta_0 + \beta_1 a_i + \beta_2 m_i + \beta_3 h_i + \beta_4 k_i + \beta_5 d_i + \beta_6 e_i + \beta_7 p_i + \beta_8 x_i + \beta_9 c_i + \beta_{10} s_i + \beta_{11} g_i$   
$\beta_0 \sim N(0, 1)$   
$\beta_j | \tilde{\lambda_j}, \tau \sim N(0, \tilde{\lambda_j} \tau)$   
$\tilde{\lambda_j} = \frac{c \lambda_j}{\sqrt{c^2+\tau^2\lambda_j^2}}$   
$\lambda_j \sim C^+(0, 1)$, $j=1, \cdots, P$   
$\tau \sim C^+(0, \tau_0)$ where $\tau_0 = \frac{p_0}{P-p_0} \frac{\sigma}{\sqrt{n}}$   
We approximate $\sigma$ with pseudo variance $\tilde{\sigma}^2=1/\mu(1-\mu)$ for non-gaussian link  
$c^2\sim Inv-Gamma(\upsilon/2, n\upsilon/2s^2)$   

1. Intuition  
2. Problem  
3. Algorithm
4. Applications 
5. Limitations



Các phương pháp giảm chiều dữ liệu:

**PCA**
1. Định nghĩa:

$$Z_c = Z - \mu; \quad C = \frac{1}{N}Z_C^T\,Z_C$$
  
2. PCA giải bài toán tìm $w \in \mathbb{R}^d$ sao cho:

$$ \max_{w} Var(Z_c \, w) $$

Đây là phép chiếu từng sample lên hướng $w$ 

Ta có:
 $$ Var(Z_c \, w) = \frac{1}{N}(Z_c \, w)^T\,(Z_c \, w) = w^T\,C\,w$$

vì có thể scale $w$ nên cho thêm constraint $\parallel w \parallel = 1$.

Giải bằng Lagrange multiplier:
$$\mathcal{L}(w, \lambda) = w^TCw - \lambda(w^Tw-1)$$

Giải đạo hàm:
$$Cw = \lambda w$$

Đây chính là eigenvalue problem

**SVD**
- TSNE
- LDA
- PLS Regression

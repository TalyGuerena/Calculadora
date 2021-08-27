// Calculadora
// Calculadora Forms C#

using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace CalculadoraForms
{
    public partial class Form1 : Form
    {
        // Variáveis necessárias para o desenvolvimento do código
        private double entrada1 = 0;
        private double entrada2 = 0;
        private int oper = 0;

        public Form1()
        {
            InitializeComponent();
        }

        private void btnClear_Click(object sender, EventArgs e)
        {
            txtResult.Text = "";
        }

        private void btn1_Click(object sender, EventArgs e)
        {
            String temp;
            temp = txtResult.Text;
            txtResult.Text = temp + "1";
        }

        private void btn0_Click(object sender, EventArgs e)
        {
            String temp;
            temp = txtResult.Text;
            if (temp.Length != 0)
                txtResult.Text = temp + "0";
        }

        private void btn2_Click(object sender, EventArgs e)
        {
            String temp;
            temp = txtResult.Text;
            txtResult.Text = temp + "2";
        }

        private void btnPonto_Click(object sender, EventArgs e)
        {
            String temp;
            temp = txtResult.Text;
            if (temp.Length != 0)
            {
                if (temp.Contains(".") == false)
                {
                    txtResult.Text = temp + ".";
                }
            }
            else 
            {
                txtResult.Text = temp + "0";
            }
        }

        private void btn3_Click(object sender, EventArgs e)
        {
            String temp;
            temp = txtResult.Text;
            txtResult.Text = temp + "3";
        }

        private void btn4_Click(object sender, EventArgs e)
        {
            String temp;
            temp = txtResult.Text;
            txtResult.Text = temp + "4";
        }

        private void btn5_Click(object sender, EventArgs e)
        {
            String temp;
            temp = txtResult.Text;
            txtResult.Text = temp + "5";
        }

        private void btn6_Click(object sender, EventArgs e)
        {
            String temp;
            temp = txtResult.Text;
            txtResult.Text = temp + "6";
        }

        private void btn7_Click(object sender, EventArgs e)
        {
            String temp;
            temp = txtResult.Text;
            txtResult.Text = temp + "7";
        }

        private void btn8_Click(object sender, EventArgs e)
        {
            String temp;
            temp = txtResult.Text;
            txtResult.Text = temp + "8";
        }

        private void btn9_Click(object sender, EventArgs e)
        {
            String temp;
            temp = txtResult.Text;
            txtResult.Text = temp + "9";
        }

        private void btnSoma_Click(object sender, EventArgs e)
        {
            if (entrada1 == 0)
            {
                entrada1 = Convert.ToDouble(txtResult.Text);
            }
            else
            {
                entrada1 = entrada1 + Convert.ToDouble(txtResult.Text);
            }
            oper = 1;
            txtResult.Text = "";
        }

        private void btnSubtrair_Click(object sender, EventArgs e)
        {
            if (entrada1  == 0)
            {
                entrada1 = Convert.ToDouble(txtResult.Text);
            }
            else
            {
                entrada1 = entrada1 - Convert.ToDouble(txtResult.Text);
            }
            oper = 2;
            txtResult.Text = "";
        }

        private void btnMultiplicar_Click(object sender, EventArgs e)
        {
            if (entrada1 == 0)
            {
                entrada1 = Convert.ToDouble(txtResult.Text);
            }
            else
            {
                entrada1 = entrada1 * Convert.ToDouble(txtResult.Text);
            }
            oper = 3;
            txtResult.Text = "";
        }

        private void btnDiv_Click(object sender, EventArgs e)
        {
            if (entrada1 == 0)
            {
                entrada1 = Convert.ToDouble(txtResult.Text);
            }
            else
            {
                entrada1 = entrada1 / Convert.ToDouble(txtResult.Text);
            }
            oper = 4;
            txtResult.Text = "";
        }

        private void btnResult_Click(object sender, EventArgs e)
        {
            double resultado;
            entrada2 = Convert.ToDouble(txtResult.Text);

            if (oper == 1)
            {
                resultado = entrada1 + entrada2;
                txtResult.Text = Convert.ToString(resultado);
            }
            if (oper == 2)
            {
                resultado = entrada1 - entrada2;
                txtResult.Text = Convert.ToString(resultado);
            }
            if (oper == 3)
            {
                resultado = entrada1 * entrada2;
                txtResult.Text = Convert.ToString(resultado);
            }
            if (oper == 4)
            {
                if (entrada2 == 0)
                {
                    txtResult.Text = "Error";
                }
                else
                {
                    resultado = entrada1 / entrada2;
                    txtResult.Text = Convert.ToString(resultado);
                }
            }
            entrada1 = 0;
            entrada2 = 0;
        }

        private void btnPerc_Click(object sender, EventArgs e)
        {
            double perc = Convert.ToDouble(txtResult.Text) / 100;
            txtResult.Text = Convert.ToString(perc);
        }

        private void btn1porX_Click(object sender, EventArgs e)
        {
            double divx = 1 / Convert.ToDouble(txtResult.Text);
            txtResult.Text = Convert.ToString(divx);
        }

        private void btnInvert_Click(object sender, EventArgs e)
        {
            double inv = (-1) * Convert.ToDouble(txtResult.Text);
            txtResult.Text = Convert.ToString(inv);
        }
    }
}

namespace Progress_Bar_Michelle_Muliawan
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
            TeksStatusBar.Text = 
                "UNIKA ATMA JAYA";
            DateStatusBar.Text = 
                DateTime.Now.ToShortTimeString ();
        }

        private void button1_Click(object sender, EventArgs e)
        {
            label2.Text = "TANGGAL: " +
                DateTime.Now.ToLongDateString();
            this.timer1.Start();
        }

        private void timer1_Tick(object sender, EventArgs e)
        {
            label1.Text = "JAM : " +
                DateTime.Now.ToLongTimeString ();
            this.progressBar1.Increment(0);
            progressBar1.PerformStep ();
            TimeStatusBar.Text = 
                DateTime.Now.ToShortTimeString ();
        }
    }
}

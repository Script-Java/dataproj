
                if contingency_value != 'None':
                    dff_post = pd.read_csv(os.path.join(
                        base_path, "post-ctg-flow.csv"))
                    dff_post = dff_post[dff_post.label == trans_id]
                    trans_x = dff_post["snapshot"]
                    trans_y = dff_post["('Line', 'ln7-8')"]
                    fig.add_trace(go.Scatter(x=trans_x, y=trans_y,
                                  mode='lines', name='post-ctg'))

 

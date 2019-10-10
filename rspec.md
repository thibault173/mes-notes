expect(subject) est équivalent à is_expected
expect{subject} est différent de expect(subject)
expext{subject}.to change(User.count) va exécuter User.count 2 fois


allow à faire dans un before de préférence

allow_any_instance_of(Demo). to receive(:aa).an_return('toto')

let(:toto) { instance_double(HHTP::Response, body: 'toto')}
